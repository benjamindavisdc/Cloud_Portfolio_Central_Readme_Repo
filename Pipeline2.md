## CI/CD Container Deployment and Configuration
This project utilizes a CI/CD (Continuous Integration/Continuous Deployment) approach to deploy and configure a website on an Apache container. The deployment process is driven by a Jenkins container and a Jenkins pipeline. The following sections provide an overview of the project's components and how they work together.

# Bootstrap.sh
This script is responsible for configuring the VM (Virtual Machine) and containers through the following steps:
> It sets up Docker and Docker Network on the host machine. Each container is built and connected to the Docker network during creation. The Jenkins container runs the pipeline, which deploys the website code from GitHub to Apache. 

> Starts the Docker service and adds the current user to the "docker" group. Additionally, it outputs the Docker version.

> updates the system and installs Jenkins on the host machine. It starts the Jenkins service and enables it to run on system startup. The script also outputs the initialAdminPassword, which is required for initial Jenkins setup. Finally, it checks the status of the Jenkins service.

> Creates a Jenkins user using the Jenkins CLI (Command Line Interface). The should be replaced with the desired username and password for the Jenkins user.

> Defines a Jenkins pipeline named "test7pipeline1" which is used for the web deployment process. The pipeline contains multiple stages that clone the Git repository, clean the web directory, copy the files to the Apache container, and perform clean-up tasks.

> Installs and configures the Apache web server on the host machine. It starts the Apache service, enables it to run on system startup, and opens the necessary firewall ports. The script also outputs the version of Apache installed.


# Apache Dockerfile
This Dockerfile builds an Apache image that includes Git, Apache, and the latest copy of the web application. It clones the repository, installs Apache, copies the repository contents to the appropriate location, and exposes port 80 for incoming HTTP traffic.

# Jenkins Dockerfile
This Dockerfile builds a Jenkins image with Java OpenJDK 11 installed. It creates a directory for the Jenkinsfile in the container, copies the Jenkinsfile to the container, and exposes ports 443 and 8080 for accessing the Jenkins server.

# Jenkinsfile for Web Deployment
This Jenkinsfile defines the pipeline stages for web deployment. It includes stages for cloning the Git repository, cleaning the web directory, copying the files to the Apache container, and cleaning up temporary files. Each stage is executed as part of the pipeline.

# Project Workflow
The bootstrap.sh script configures the VM and sets up Docker and Docker Network.
The Jenkins container is created using the Jenkins Dockerfile.
The Apache container is created using the Apache Dockerfile.
The Jenkins container runs the Jenkins pipeline (test7pipeline1) for web deployment.
The pipeline stages are executed, which clone the Git repository, clean the web directory, copy the files to the Apache container, and perform clean-up tasks.
The website is deployed on the Apache container and hosted on port 80.
The Jenkins container continues to monitor for changes in the Git repository and triggers pipeline execution when new changes are detected.
