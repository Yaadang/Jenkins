# Jenkins CI/CD Pipeline Projects
  This repository contains several demo projects that demonstrate how to set up and use Jenkins to build, test, and deploy software applications using a continuous integration and continuous deployment (CI/CD) pipeline.

## Technologies Used
    The following technologies are used in these projects:
    - Jenkins
    - Docker
    - DigitalOcean
    - Linux
    - Git
    - Java
    - Maven
    - Groovy
    - Github

# Projects
The following projects are included in this repository:

## Install Jenkins on DigitalOcean
    Project Description:
    Create an Ubuntu server on DigitalOcean Set up and run Jenkins as Docker container Initialize Jenkins

## Build Automation & CI/CD with Jenkins
    Project Description: 
    CI Pipeline for a Java Maven application to build and push to the repository

    Install Build Tools (Maven, Node) in Jenkins
    Make Docker available on Jenkins server
    Create Jenkins credentials for a git repository
    Create different Jenkins job types (Freestyle, Pipeline, Multibranch pipeline) for the Java Maven project with Jenkinsfile to:
    Connect to the application’s git repository
    Build Jar
    Build Docker Image
    Push to private DockerHub repository
   
##  Demo Project: Create a Jenkins Shared Library
    Create a Jenkins Shared Library to extract common build logic:
    Create separate Git repository for Jenkins Shared Library project
    Create functions in the JSL to use in the Jenkins pipeline
    Integrate and use the JSL in Jenkins Pipeline (globally and for a specific project in Jenkinsfile)

## Configure Webhook to trigger CI Pipeline automatically on every change
    Project Description:

    Install GitLab Plugin in Jenkins
    Configure GitLab access token and connection to Jenkins in GitLab project settings
    Configure Jenkins to trigger the CI pipeline, whenever a change is pushed to GitLab
    
## Dynamically Increment Application version in Jenkins Pipeline
    Project Description:
    Configure CI step: Increment patch version
    Configure CI step: Build Java application and clean old artifacts
    Configure CI step: Build Image with dynamic Docker Image Tag
    Configure CI step: Push Image to private DockerHub repository
    Configure CI step: Commit version update of Jenkins back to Git repository
    Configure Jenkins pipeline to not trigger automatically on CI build commit to avoid commit loop
