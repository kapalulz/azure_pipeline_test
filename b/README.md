# codebuild-demo-webpage
This repository demonstrates the use of AWS CodeBuild to automate the build and deployment process of a web application. The project consists of the following key components:

**Dockerfile:**

    FROM nginx:latest

    COPY ./index.html   /usr/share/nginx/html/index.html
    COPY ./awslogo.png  /usr/share/nginx/html/awslogo.png

**buildspec.yml:**
The buildspec.yml file defines the AWS CodeBuild build and deployment process. It specifies the environment variables, 
Docker image tagging, and other build steps are required to package and deploy your application to Amazon Elastic Container Registry (ECR).

index.html that will be served by the Nginx web server in the Docker container.

*githook connected to AWSBuild
![image](https://github.com/kapalulz/pipeline-aws_codebuild-webpage/assets/17459523/f08ca10a-4026-465d-8fe3-b2bab331f68f)


<img src="https://cdn.discordapp.com/attachments/1146494704519761992/1146531589346570390/Web_page.gif">
