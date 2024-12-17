# RHEL-Migration-Commands

# Command to export an container
https://docs.docker.com/reference/cli/docker/container/export/ <br>

```
# This is write the container to a tar file of your choice
docker export <name-of-stopped-container> > <my-tar-file>

# Import this to a new image
docker import <my-tar-file> <name-of-restored-image>

# Spin up a new container using this image
docker run <name-of-restored-image>

```
