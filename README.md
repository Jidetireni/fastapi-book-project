# **FastAPI Book Management API**

## **Overview**

This project is a RESTful API built with **FastAPI** for managing a book collection. It provides comprehensive **CRUD (Create, Read, Update, Delete) operations** with proper error handling, input validation, and auto-generated documentation.

To ensure a seamless development and deployment workflow, the project includes a **CI/CD pipeline** for automated testing, building, and cloud deployment. Additionally, **DNS and SSL certificates** have been configured for secure access.

## **Implementation Summary**

### 1. **API Development**  
   - Implemented a `GET /books/{id}` endpoint to retrieve a specific book by its ID.  

### 2. **Continuous Integration (CI) Pipeline**  
   - Configured **GitHub Actions** to automatically **build and test** the application on each pull request to the `main` branch.

### 3. **Containerization & Reverse Proxy**  
   - Created a **Dockerfile** to containerize the application.  
   - Configured **Nginx** as a **reverse proxy** for efficient request handling.  
   - Used **Docker Compose** to manage both the API and Nginx services.

### 4. **Security & Networking**  
   - Integrated **DNS** for domain name resolution.  
   - Configured **SSL certificates** to enforce secure HTTPS connections.

### 5. **Continuous Deployment (CD) Pipeline**  
   - Automated the deployment process with CI/CD:  
     - Built and pushed the API image to **Docker Hub**.  
     - Established an **SSH-based deployment strategy**:  
       - SSH into the cloud instance.  
       - Pull the latest code repository.  
       - Run `docker compose up` to deploy the latest version.
