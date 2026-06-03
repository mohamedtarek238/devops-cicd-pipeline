# Technical Decisions

## Project Goal

Build a complete CI/CD pipeline using Jenkins and Docker.

## Why Jenkins

- Industry standard
- Large plugin ecosystem
- Easy Docker integration

## Why Docker

- Consistent deployments
- Containerized workloads
- Industry adoption
# Technical Decisions

## Jenkins Deployment Strategy

Jenkins was deployed as a Docker container instead of a system service.

## Custom Jenkins Image

A custom Jenkins image was selected to include:

* Docker CLI
* Git
* CI/CD tooling

Reason:

This approach allows Jenkins pipelines to build and deploy Docker containers while keeping Jenkins itself containerized.
# Technical Decisions

## Why Containerized Jenkins

Jenkins was deployed as a container instead of a system service.

Benefits:

* Portability
* Easy upgrades
* Consistent runtime environment

## Why Docker Socket Mounting

The Docker socket was mounted into the Jenkins container to allow pipeline execution of Docker commands.

## Why a Custom Jenkins Image

A custom Jenkins image was built to include:

* Docker CLI
* Git
* Additional CI/CD tooling

This allows Jenkins pipelines to interact directly with the Docker daemon.
