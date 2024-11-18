Here’s the updated and fully detailed README with all the additional instructions incorporated:

---

# Full-Stack FastAPI and React Template - DevOps November CV Challenge

Welcome to the **Full-Stack FastAPI and React Template** repository! This project serves as a demo application for the **DevOps November Resume Challenge**, where participants will deploy a full-stack application with a **FastAPI** backend and **ReactJS** frontend using **ChakraUI**. Additionally, participants will set up monitoring and logging tools, configure a reverse proxy, and deploy the application to a cloud platform, showcasing their end-to-end DevOps skills.

---

## Challenge Overview

As part of this challenge, your primary goal is to:

1. Dockerize a full-stack application with a FastAPI backend and React frontend.
2. Configure and deploy monitoring and logging tools.
3. Set up a reverse proxy for application routing.
4. Deploy the application to a cloud platform with proper domain configuration.
5. Submit a working repository with detailed documentation and screenshots of your deployed application.

---

## Challenge Requirements

1. **Dockerization**:  
   - Write `Dockerfile`s to containerize both the **React frontend** and **FastAPI backend**.  
   - Ensure each service can be built and run locally in their respective containers.  
   - Use a `docker-compose.yml` file to orchestrate all services, including the database, monitoring, and logging tools.

2. **Reverse Proxy Configuration**:  
   Configure **Traefik** or **Nginx Proxy Manager** to:  
   - Serve the frontend and backend on the same host machine port (80).  
   - Serve the **frontend** on the root path (`/`).  
   - Proxy `/api` on the backend to `/api` on the main domain.  
   - Proxy `/docs` on the backend to `/docs` on the main domain.  

3. **Database Configuration**:  
   - Use PostgreSQL as the database for the FastAPI backend.  
   - Ensure the database is properly set up and connected in the `docker-compose.yml`.  
   - Test database connectivity and functionality by running a sample API request.  

4. **Adminer Setup**:  
   - Add **Adminer** to the `docker-compose.yml` to manage the PostgreSQL database.  
   - Expose Adminer on port `8080` and configure it to be accessible via `db.domain`.  

5. **Proxy Manager Setup**:  
   - Add **Nginx Proxy Manager** or **Traefik** to the `docker-compose.yml` for managing proxy configurations.  
   - Expose the proxy manager on port `8090` and make it accessible via `proxy.domain`.  

6. **Monitoring and Logging Tools**:  
   - Deploy **Prometheus**, **Grafana**, **Loki**, and **Promtail** using `docker-compose.yml`.  
   - Configure:  
     - Prometheus to scrape application metrics.  
     - Grafana to visualize metrics and logs.  
     - Loki and Promtail to aggregate and forward logs.  
   - Ensure all monitoring and logging services are running correctly and accessible via their respective URLs.  

7. **Cloud Deployment**:  
   - Deploy the fully containerized application stack to an AWS EC2 instance (or any other cloud platform of your choice).  
   - Set up a domain for your application.  
   - If you do not have a domain, obtain a free subdomain from [Afraid DNS](https://freedns.afraid.org/).  
   - Configure:  
     - HTTP to redirect to HTTPS.  
     - `www` to redirect to the non-`www` version of your domain.  

8. **Article**:
   - Write and publish a detailed **Article** about the project. Your article should include:  
     - An overview of the project and its purpose.  
     - Step-by-step instructions on how you containerized, orchestrated, and deployed the application.  
     - Screenshots of your setup, including:  
       - The deployed application.  
       - Grafana dashboards showing metrics and logs.  
       - Reverse proxy configuration.  
     - Challenges you faced and how you resolved them.  
     - Lessons learned and tips for others.  
   - Include the link to your article in your submission.

---

## Project Structure

The repository is organized as follows:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory includes its own README file with detailed instructions:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)

---

## Getting Started

### Clone the Repository

Start by cloning this repository to your local machine:

```bash
git clone <repository-url>
cd <repository-folder>
```


## Testing and Evaluation

Your hosted application will be evaluated based on the following criteria:  

1. **Dockerization**:  
   - Verify that the `Dockerfile`s and `docker-compose.yml` work seamlessly to build and run the application.  

2. **Reverse Proxy**:  
   - Confirm that the application routes are correctly configured (frontend on `/`, backend `/api`, and backend docs `/docs`).  

3. **Database Setup**:  
   - Ensure PostgreSQL is properly configured and Adminer is accessible via `db.domain`.  

4. **Monitoring and Logging**:  
   - Test Prometheus, Grafana, Loki, and Promtail to ensure metrics and logs are being captured and displayed.  

5. **Cloud Deployment**:  
   - Confirm the application is deployed to the cloud and accessible via a public URL.  
   - Check that HTTP redirects to HTTPS, and `www` redirects to the non-`www` domain.  

6. **Repository Validation**:  
   - Verify that running `docker-compose up -d` from your repository correctly deploys the application and all supporting services.  

7. **Article**:  
   - Evaluate the clarity, detail, and technical depth of the published article.  


---

## Submission Guidelines

1. Deploy the application stack and ensure all services are running correctly.  
2. Submit the following:  
   - A link to your **GitHub repository** containing all files (`Dockerfile`, `docker-compose.yml`, configurations, etc.).  
   - A link to your **Article**.  
   - Screenshots of:  
     - The deployed application.  
     - Metrics and logs displayed in Grafana.  
     - Reverse proxy routes and configurations.  

3.  Use the provided [submission form](#) to share your work.

---

Good luck with your DevOps November CV Challenge! This is your opportunity to showcase your end-to-end DevOps skills and stand out to potential employers.