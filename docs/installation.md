# Installation Guide

## Environment

OS:
CentOS Stream 10

Docker:
Docker Engine 29.5.2

Git:
Git 2.47.3

## Jenkins Deployment

A Jenkins container was deployed using Docker.

Docker Volume:

* jenkins_home

Docker Socket:

* /var/run/docker.sock

Published Ports:

* 8080
* 50000

## Application Deployment

A sample web application was created using:

* Nginx
* HTML

Docker image build:

docker build -t devops-demo:v1 .

Container deployment:

docker run -d --name devops-demo -p 8081:80 devops-demo:v1
