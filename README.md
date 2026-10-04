# Jenkins CI/CD Pipeline

## Objective

The objective of this project is to create a simple CI/CD pipeline using Jenkins and Docker.

## Tools Used

- Jenkins
- Docker
- Git
- GitHub
- Nginx

## Project Structure

- index.html - Simple web application
- Dockerfile - Docker image configuration
- Jenkinsfile - Jenkins CI/CD pipeline
- README.md - Project documentation

## Pipeline Stages

1. Build
2. Test
3. Deploy

## CI/CD Flow

GitHub → Jenkins → Build → Test → Docker → Deploy

## Application

The application is a simple HTML page served using Nginx.

## Result

The Jenkins pipeline automatically builds the Docker image, tests the application and deploys the Docker container.