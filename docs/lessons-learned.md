# Lessons Learned

## GitHub Authentication

GitHub no longer supports password authentication for Git operations.

Solution:
- Created Personal Access Token (PAT)
- Used token for repository access
# Lessons Learned

## Docker Socket vs Docker CLI

Mounting the Docker socket alone is not sufficient for running Docker commands inside a container.

Requirements:

1. Docker daemon access through `/var/run/docker.sock`
2. Docker CLI installed inside the container

Both components are required for Jenkins pipelines that manage Docker workloads.
