# Full-Stack FastAPI and React Template - DevOps November CV Challenge

Welcome to the Full-Stack FastAPI and React template repository. This repository serves as a demo application for the **DevOps November Resume Challenge**. Participants will set up and run a full-stack application with a FastAPI backend and a ReactJS frontend using ChakraUI. and set up a monitoring and logging stack to demonstrate their DevOps skills.

## Challenge Overview

As part of the **Resume Challenge**, your task is to deploy this full-stack application on a server of your choice and configure monitoring and logging tools. You'll be responsible for writing a `Dockerfile` and `docker-compose.yml` to containerize the app and make it production-ready.
## Project Structure

The repository is organized into two main directories:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory has its own README file with detailed instructions specific to that part of the application.

## Getting Started

To get started with this template, please follow the instructions in the respective directories:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)


## Challenge Requirements

1. Write your own `Dockerfile` for each application component.
2. Create a `docker-compose.yml` file to orchestrate the services.
3. Deploy the app on a server provisioned on your chosen cloud platform (AWS, Azure, or GCP).
4. Configure monitoring tools:
   - **Prometheus**: Collect metrics.
   - **Grafana**: Visualize metrics.
   - **Loki** and **Promtail**: Aggregate and forward logs.
5. Ensure all components are accessible and monitored.

---

## Submission Guidelines

1. Deploy the app and monitoring stack.
2. Submit a link to a document with:
   - Screenshots of the deployed app.
   - Metrics and logs displayed on Grafana.
   - Details of your `Dockerfile` and `docker-compose.yml` configurations.
3. Use the provided [submission form](#).

---

## Getting Started

### Clone the Repository
```bash
git clone <repository-url>
