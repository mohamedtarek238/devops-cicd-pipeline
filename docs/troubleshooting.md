# Troubleshooting

## Issue: Docker CLI Not Available Inside Jenkins Container

### Problem

After deploying Jenkins as a Docker container and mounting the Docker socket:

```bash
-v /var/run/docker.sock:/var/run/docker.sock
```

Docker commands were not available inside the Jenkins container.

### Error

```bash
docker: command not found
```

### Root Cause

The Jenkins container had access to the Docker daemon socket but did not include the Docker CLI binary.

### Solution

A custom Jenkins image was created with Docker CLI installed.

### Outcome

Jenkins pipelines can now execute Docker build, run, stop, and remove commands directly.
