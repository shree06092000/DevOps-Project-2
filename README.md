# DevOps-Project-2
DevOps Lifecycle Implementation for Analytics Pvt Ltd


⚙️ DevOps Lifecycle Implementation for Analytics Pvt Ltd

📖 Project Overview

This project demonstrates the complete implementation of a DevOps Lifecycle for Analytics Pvt Ltd, a product-based organization that leverages Docker for containerization. With the product gaining significant traction post-launch, the company required a robust platform to automate deployment, scaling, and operations of application containers across clusters of hosts.

The solution integrates Git workflow, AWS CodeBuild, Docker, Kubernetes, Jenkins, Terraform, and configuration management tools to deliver a modern, scalable, and automated DevOps pipeline — without altering the existing Docker containers in the testing environment.

Source Code: hshar/website

🎯 Objectives

    Implement a Git workflow with controlled monthly releases (25th of every month).
    
    Automate builds and tests using AWS CodeBuild triggered on commits to the master branch.
    
    Containerize the application with a custom Dockerfile and push images to Docker Hub.
    
    Deploy the containerized application on a Kubernetes cluster with:
    
        2 replicas for high availability.
        
        NodePort service configured on port 30008.
    
    Define a Jenkins Pipeline with automated jobs for build, test, and deployment.
    
    Use configuration management to install required software across worker nodes.
    
    Provision infrastructure on AWS using Terraform.

🛠️ Solution Architecture
    Version Control & Git Workflow
    
        Monolithic architecture managed with Git.
        
        Controlled release cycle (25th of every month).
    
    Continuous Integration (AWS CodeBuild)
    
        Triggered automatically on commits to the master branch.
        
        Executes build and test stages before deployment.
    
    Containerization (Docker)
    
        Custom Dockerfile created for the application.
        
        Images built and pushed to Docker Hub on every GitHub push.
        
        Application code resides in /var/www/html.
    
    Orchestration (Kubernetes)
    
        Deployed containerized application with 2 replicas.
        
        NodePort service configured on port 30008.
    
    CI/CD Pipeline (Jenkins)
    
        Pipeline jobs defined:
        
            Job1: Build – Builds Docker image and prepares artifacts.
            
            Job2: Test – Runs automated tests.
            
            Job3: Prod – Deploys to Kubernetes cluster.
    
    Configuration Management
    
        Automated installation of required software on worker nodes:
        
            Worker1: Jenkins, Java
            
            Worker2: Docker, Kubernetes
            
            Worker3: Java, Docker, Kubernetes
            
            Worker4: Docker, Kubernetes
    
    Infrastructure as Code (Terraform)
    
        Provisioned AWS infrastructure for scalable deployments.
        
        Automated cluster creation and resource allocation.

🔒 Security & Best Practices
    
    IAM roles and policies applied for least-privilege access.
    
    Secure communication via HTTPS.
    
    Automated builds reduce manual intervention.
    
    Kubernetes ensures scalability and resilience.

📈 Key Features

    Automated CI/CD pipeline with Jenkins and AWS CodeBuild.
    
    Custom Docker images built and pushed to Docker Hub.
    
    Kubernetes deployment with replicas and NodePort service.
    
    Infrastructure automation using Terraform.
    
    Configuration management for consistent environments.

🚀 Future Enhancements

    Implement Helm charts for Kubernetes deployments.
    
    Add CloudWatch monitoring for proactive alerts.
    
    Enable Blue/Green or Canary deployments for zero-downtime releases.
    
    Integrate SonarQube for code quality analysis.

📌 Impact

This project showcases how a DevOps Lifecycle can transform a monolithic architecture into a scalable, automated, and cloud-native solution. It highlights expertise in CI/CD pipelines, containerization, orchestration, infrastructure automation, and cloud deployment — ensuring faster releases, high availability, and operational efficiency.
