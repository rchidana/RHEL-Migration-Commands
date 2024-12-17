# RHEL-Migration-Commands

# Command to export an container
https://docs.docker.com/reference/cli/docker/container/export/ <br>

```

# First inspect the running container to check if any specific volume, command, ports & other configurations are used while spinning up this container
docker inspect <your-orig-container>

# Back up any volumes and recreate them in the new node

# Stop your container so that you can export it to a tar file
docker stop <your-orig-container>
# This is write the container to a tar file of your choice
docker export <your-orig-container> > <my-tar-file>

# Import this to a new image
docker import <my-tar-file> <name-of-restored-image>

# Spin up a new container using this image
docker run <name-of-restored-image>

```
