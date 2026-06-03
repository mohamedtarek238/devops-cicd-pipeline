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
