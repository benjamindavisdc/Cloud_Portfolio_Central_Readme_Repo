## Automated Infrastructure Blueprint
This project showcases an automated infrastructure blueprint for building a server and database using AWS. The code is stored in CodeCommit and is displayed live on my portfolio site. It leverages Terraform for provisioning and managing the infrastructure resources. The blueprint consists of multiple components working together to create a fully functional system. Below is an overview of each component and its purpose.

# Main.tf
This folder contains the Terraform configuration files (main.tf) responsible for provisioning the basic infrastructure. It includes the AWS provider configuration, DynamoDB table creation, and the module for creating a VPC. The VPC module sets up a virtual private cloud with public and private subnets.

# SG.tf
The SG.tf file defines the security groups and SSH keys required for the infrastructure. It creates security group rules to allow web traffic (port 8080), SSH traffic (port 22), and HTTP traffic (port 80). Additionally, it sets up a security group for private traffic over TLS (port 443) and creates an SSH key pair for remote server access.

# Lambda.tf
The Lambda.tf file defines the AWS Lambda function and its dependencies. It sets up an S3 bucket for storing the Lambda function code and creates the necessary IAM roles and policies. The Lambda function is event-driven and triggered whenever the source code is updated. It performs the scraping of repositories and interacts with DynamoDB to store and retrieve data.

# buildspec.yml
The buildspec.yml file is an automated deployment script that provides instructions to AWS CodeBuild on how to build the Terraform configuration. It defines the steps and commands for deploying the infrastructure using the Terraform files. The script is triggered when code is pushed to AWS CodeCommit, and it orchestrates the deployment process.

By following this automated infrastructure blueprint, you can easily provision and manage your server and database resources on AWS. The Terraform configuration ensures consistency and scalability, while the Lambda function enables seamless updates and data processing.
