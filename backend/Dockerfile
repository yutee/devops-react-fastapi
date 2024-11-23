# Build stage
FROM python:3.10-slim as builder

# Install poetry
RUN pip install poetry

# Copy only requirements to cache them in docker layer
WORKDIR /app
COPY poetry.lock pyproject.toml /app/

# Configure poetry
RUN poetry config virtualenvs.create false \
    && poetry install --no-interaction --no-ansi --no-root --no-dev

# Final stage
FROM python:3.10-slim

# Create app directory
WORKDIR /app

# Install PostgreSQL client
RUN apt-get update \
    && apt-get install -y libpq-dev gcc \
    && rm -rf /var/lib/apt/lists/*

# Copy Python dependencies from builder stage
COPY --from=builder /usr/local/lib/python3.10/site-packages/ /usr/local/lib/python3.10/site-packages/
COPY --from=builder /usr/local/bin/ /usr/local/bin/

# Copy application code
COPY . /app

# Create a non-root user
RUN adduser --disabled-password --gecos "" appuser
RUN chown -R appuser:appuser /app
USER appuser

# Set environment variables
ENV PYTHONPATH=/app
ENV PORT=8000

# Run the prestart script and start the application
CMD ["sh", "-c", "bash ./prestart.sh && uvicorn app.main:app --host 0.0.0.0 --port $PORT"]

# Expose the port the app runs on
EXPOSE 8000