# MLflow and DVC with CICD Deployment on AWS

## Workflows

    1. update config.yaml
    2. update params.yaml
    3. update the entity
    4. update the configuration manager in src config
    5. update the components
    6. update the pipeline
    7. update the main.py
    8. update the app.py

## MLflow and dagshub

```bash
MLFLOW_TRACKING_URI=https://dagshub.com/shahed9338/MLflow-and-DVC-with-CICD-Deployment-on-AWS.mlflow\
```

## DVC cmd

```bash
1. dvc init
2. dvc repro
3. dvc dag
```

# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

```bash
#with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
```

## 3. Create ECR repo to store/save docker image

## 4. Create EC2 machine (Ubuntu)

## 5. Open EC2 and Install docker in EC2 Machine:


```bash
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```
## 6. Configure EC2 as self-hosted runner:

```bash
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```
## 7. Setup github secrets:

```bash
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = 

AWS_ECR_LOGIN_URI = 

ECR_REPOSITORY_NAME = 
```
