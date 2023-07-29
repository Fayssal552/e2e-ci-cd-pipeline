# End to End CI CD Pipeline
Once the CI/CD pipeline is set up, any new code commits pushed to the `main` branch on GitHub will trigger the pipeline. Jenkins will build the application, and SonarQube will analyze the code quality. The Docker image will be pushed to DockerHub, and Argo CD will automatically deploy the application to your Kubernetes cluster.

-  Blog Link : [Installation and Usage Guide](https://victorious-peace-7a9.notion.site/E2E-CI-CD-Pipeline-e1d67b9b5c2a4189a32f7f097eadd591?pvs=4).

![Diapositive1.JPG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b4c43794-2fc2-4bd4-8f4a-d500bf519a92/Diapositive1.jpg)

# Project Description

The project involves building and deploying a Java application using a CI/CD pipeline. The following steps are involved in the process:

1. **Version Control**: The code is stored in a version control system such as Git, and hosted on GitHub. 

2. **Continuous Integration**: [Jenkins](https://jenkins.io/) is used as the CI server to build the application. Whenever there is a new code commit, Jenkins automatically pulls the code from GitHub and builds it using Maven.

3. **Code Quality**: [SonarQube](https://www.sonarqube.org/) is used to analyze the code and report on code quality issues such as bugs, vulnerabilities, and code smells. The SonarQube analysis is triggered as part of the Jenkins build pipeline.

4. **Containerization**: [Docker](https://www.docker.com/) is used to containerize the Java application. The Dockerfile is stored in the Git repository along with the source code. The Dockerfile specifies the environment and dependencies required to run the application.

5. **Container Registry**: The Docker image is pushed to [DockerHub](https://hub.docker.com/), a public or private Docker registry. The Docker image can be versioned and tagged for easy identification.

6. **Continuous Deployment**: [Argo CD](https://argoproj.github.io/argo-cd/) is used to automate the deployment of the containerized application to Kubernetes. Whenever a new version of the application image is pushed to the Git repository, Argo CD will automatically deploy it to the Kubernetes cluster.

## Installation and Usage Guide

For detailed instructions on how to install and run the project, please refer to our [Installation and Usage Guide](https://victorious-peace-7a9.notion.site/E2E-CI-CD-Pipeline-e1d67b9b5c2a4189a32f7f097eadd591?pvs=4).


