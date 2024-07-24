## Containerisation and Deployment of Wisecow Application on Kubernetes

## Objective
To containerize and deploy the Wisecow application, hosted in the GitHub repository (https://github.com/nyrahul/wisecow), on a Kubernetes environment with secure TLS communication.

## Dockerization
Develop a Dockerfile for creating a container image of the Wisecow application.

## Kubernetes Deployment
Craft Kubernetes manifest files for deploying the Wisecow application in a Kubernetes environment.
The Wisecow app must be exposed as a Kubernetes service for accessibility.

## Continuous Integration and Deployment (CI/CD)
Implement a GitHub Actions workflow for:
Automating the build and push of the Docker image to a container registry whenever changes are committed to the repository.
Continuous Deployment [Challenge Goal]: Automatically deploy the updated application to the Kubernetes environment following successful image builds.

## TLS Implementation [Challenge Goal]
Ensure that the Wisecow application supports secure TLS communication.

## 1. Dockerization
    Created a Dockerfile for the Wisecow application.
    
## 2. Kubernetes Deployment
Deployment Manifest:
    Created deployment.yaml for Kubernetes Deployment.
Service Manifest:
    Created service.yaml for Kubernetes Service.

## 3. Continuous Integration and Deployment (CI/CD)
GitHub Actions Workflow
    Created .github/workflows/ci-cd.yml for CI/CD

## 4. TLS Implementation
  To enable secure TLS communication, configure the Ingress resource in Kubernetes with TLS certificates. This ensures that all traffic to the Wisecow application is encrypted.
Ingress Manifest for TLS
    Created ingress.yaml for Kubernetes Ingress with TLS

## Setup and Usage
1.Clone the repository:
    git clone https://github.com/nyrahul/wisecow.git
    cd wisecow
    
2.Build the Docker image:
    docker build -t <your-container-registry>/wisecow:latest .
    
3.Push the Docker image to your registry:
    docker push <your-container-registry>/wisecow:latest

4.Deploy to Kubernetes:
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
    kubectl apply -f ingress.yaml






