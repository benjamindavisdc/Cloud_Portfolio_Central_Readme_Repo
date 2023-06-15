## Cloud Engineer Portfolio - Backend Infrastructure
Welcome to a guided tour of this Cloud Backend Infrastructure portfolio. This project showcases my skills as an AWS Certified Cloud Engineer and consists of three distinct, automated pipelines that leverage popular DevOps services to build, modify, and duplicate the project seamlessly.

## Pipeline 1: Automated Cloud Infrastructure Blueprint
Infrastructure as Code
The first step in creating this project was designing the backend infrastructure. I employed the following technologies and tools:

Terraform: Used to define the infrastructure as code.
AWS CodeCommit: Serves as the code repository for storing the infrastructure code.
AWS CodePipeline: Enables the automatic deployment of infrastructure changes.
YAML scripting: Used to configure the deployment pipeline.
The infrastructure blueprint encompasses files such as main.tf, sg.tf, lambda.tf, SSH keys, and supporting files. By updating the code repository on AWS, the infrastructure is automatically deployed. This folder encompasses the control over compute, database, security, and web app infrastructure.


## Pipeline 2: CI/CD Container Deployment Pipeline
After deploying the server, it needs to be configured to host containers. I automated this process using bootstrap scripts, Dockerfiles, and Jenkinsfiles to perform important tasks, including:

Installing Docker
Installing Jenkins
Installing Apache
Building a Docker Network
Building a Jenkins Image and Container
Building an Apache Image and Container
Initializing Jenkins
Initializing Apache
Configuring the Jenkins Pipeline job from a Jenkinsfile
Delivering repository files to the Apache web server directory

[Explore the Code Repository](https://github.com/your-username/your-repo](https://github.com/benjamindavisdc/may23pipeline01)

## Pipeline 3: X-Ray App - Full Stack Python REST API
To showcase the backend infrastructure over the internet, I developed a unique full-stack app. The X-Ray App consists of two parts:

Data Scraping: The app scrapes repositories and stores the data in DynamoDB.
Data Visualization: The app displays the stored data as HTML using Python Flask.
Traditional portfolio websites often fail to demonstrate the backend aspects of work. To overcome this limitation, I created the X-Ray App to allow visitors to delve into my infrastructure code and gain a deeper understanding of my expertise.

[Explore the Code Repository](https://github.com/your-username/your-repo](https://github.com/benjamindavisdc/lambdaRepoScrapers/blob/main/jenkinsf_scraper.py)

# Services Used
Throughout this project, I utilized various services and technologies to ensure effective deployment and management:

Docker: Enables containerization of the pipeline and web hosting within a single VM.
Terraform: Provides resource management and ensures all necessary components are in place.
Jenkins: Ensures the web server is always up to date with the latest changes.
Apache: Managed through bash scripts in part 2 for efficient configuration.
AWS Services: EC2, ALB, ASG, Firewalls, and Policies facilitate seamless communication and pipeline creation.
DynamoDB: Stores the backend code, which is then visualized on the frontend.
Lambda: Monitors code changes and updates the code stored in the database.
Bash Scripts: Specified which files to include and how they should be stored.
Flask: Transformed the entire website into an app, integrating dynamic content into the HTML.

# About Me
I am a passionate Cloud Engineer with expertise in System Administration, Full Stack Web Development, and extensive experience in the Healthcare field.

If you have any questions or would like to learn more, please don't hesitate to reach out!
