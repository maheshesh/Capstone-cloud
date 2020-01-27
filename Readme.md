CloudDevops project.CI/CD pipeline to create a cluster in EKS and deploy a simple web app in Kubernetes.

**Install:
Use this CI/CD pipeline we will need:
* Jenkins
* eksctl
* aws cli
* docker
* kubectl

**Jenkins Installation
* Installed on an EC2 machine
* Configured GIT and AWS credentials for Jenkins
* Jenkins 2.204.1 was installed on the EC2

**Pipelines:
Two pipelines are setup in Jenkins
1) Creating the EKS cluster using eksctl-cloudformation
2) Blue-green deployment pipeline


**Pipeline-1: Create Cluster
* Using eksctl command: This one is quite straightforward, please ensure you have a eksAdminRole created and attached to EKS 

**Pipeline-2: Deploy (Lint, Docker image creation, Deploy to Blue->Approve->Deploy to Green)
* Please refer to the Jenkins file stages you will get to understand the various stages
* Things to note: 
*   Ensure that the kubectl, awsclient and python versions are correct
*   I installed aws-cli/1.17.9 Python/2.7.17 Linux/4.15.0-1057-aws botocore/1.14.9
*   in the /usr/local/bin/aws ubuntu instance
* Blue & Green deployment
* Validate your deployment by using kubectl get Pods and ensure your kubeconfig is set properly 
* you can view it by kubectl config view

** Debug and debug
* And EKS is fun!!!

