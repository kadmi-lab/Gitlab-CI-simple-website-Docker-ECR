# Build and deploy a Docker image to Amazon ECR using GitLab CI/CD:

## Prerequisites

1. A GitLab account
2. A GitLab repository that contains the source code for the application
3. An Amazon Web Services (AWS) account
4. A Dockerfile that describes how to build the Docker image for the application
5. New user AWS with AmazonEC2ContainerRegistryPowerUser access.

## Step 1: Set up an Amazon ECR repository

1. Go to the AWS Management Console and navigate to Amazon ECR.
2. Create a new repository for the Docker image.
3. Note down the URL of the repository, as you will need it later in the GitLab CI/CD pipeline.

## Step 2: Create a GitLab CI/CD pipeline

1. In the GitLab repository, create a new file named .gitlab-ci.yml.
2. Edit file code variables.
3. Replace <ECR-REPOSITORY-URL> with the URL of the Amazon ECR repository you created in Step 1.
4. Replace <AWS-REGION> with the region of your Amazon ECR repository.
5. Replace <APP-NAME> with the name of your application.
6. Copy created AWS user Access and Secret key to Gitlab Project settings Variables section with Key:
AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY

## Step 3: Build and push the Docker image

1. Commit and push the changes to the GitLab repository.
2. GitLab CI/CD will automatically start running the pipeline defined in .gitlab-ci.yml.
3. The pipeline will build the Docker image using the Dockerfile in the repository and push it to the Amazon ECR repository you specified.
4. Once the pipeline is complete, you can go to the Amazon ECR repository to see the Docker image that was pushed.

You have successfully built and deployed a Docker image to Amazon ECR using GitLab CI/CD. 
Potentially you can now use this Docker image to deploy your application to a Kubernetes cluster or other container orchestration platform.
