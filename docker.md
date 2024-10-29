---
layout: default
permalink: /docker/
title:  Stanford AHA
---
# Using Docker to Run the AHA Flow

[Docker Overview](https://docs.docker.com/guides/docker-overview/) :: 
<https://docs.docker.com/guides/docker-overview/>

# Install Docker

```
sudo systemctl start docker
```

On Linux systems you will need to use `sudo` to run all docker commands (`sudo docker`) unless you add your user to the `docker` group. To add your user to the `docker` group run the following:
```
sudo usermod -aG docker ${USER}
```

Then you need to logout and log back in and after that you can verify you are part of the `docker` group by running `groups`.

# Download the Docker image

The Docker image for this tutorial is available on DockerHub as 
[stanfordaha/garnet](https://hub.docker.com/r/stanfordaha/garnet/).
We will be using the one tagged `stanfordaha/garnet:latest` (about 6-8 GB in size).

Download the Docker image by running the following command (on Windows 10 you should run it in the PowerShell).
```
docker pull stanfordaha/garnet:latest
```
You may need to add login credentials to be able to pull. In that case you can add your credentials by running the following. A prompt will ask for your password as well.
```
docker login -u <your-dockerhub-username>
```

# Start the Docker container

## Linux

In Linux, you should be able to launch the container by doing this
```
container_name=any-name-you-like
docker run -it -d --name ${container_name} stanfordaha/garnet:latest bash
```
<!-- THIS IS COMMENTED OUT
Or, if that doesn't work so well, you can try this more complicated invocation, copied from the ESP tutorial (see "Attribution" section below). This command specifically includes security-opt and network arguments, and also maybe allows X connections from inside the container(?)
```
docker run -it --name ${container_name} \
  --security-opt label=type:container_runtime_t --network=host \
  -e DISPLAY=$DISPLAY -v "$HOME/.Xauthority:/root/.Xauthority:rw" \
  stanfordaha/garnet:latest /bin/bash
```
-->

## MacOS and Windows 10

The [ESP tutorial](https://esp.cs.columbia.edu/tutorials/isca2024/docker/) has instructions for starting a container on MacOS and Windows, but most of the compexity seems to involve communicating with an X server, which we don't do. For our purposes, you should probably be able to use the same Linux `docker run` command as shown above, in a command or powershell window.

# Useful Docker commands
```
docker images                 # List all local images
docker rmi <image-name>       # Delete an image

docker ps -a                  # List all local containers and their IDs
docker stop   <container-ID>  # Stop a container
docker start  <container-ID>  # Start a container
docker attach <container-ID>  # Attach to a running container
docker rm -f  <container-ID>  # Delete a container

# Copy data from host machine to a container
docker cp <path-on-host> <container-ID>:/<path-inside-container>

# Copy data from container to host machine
docker cp <container-ID>:/<path-inside-container> <path-on-host>

# Exit a container (do this from *inside* the container)
exit   
```
Complete Docker documentation can be found here: <https://docs.docker.com/>


## Attribution

This tutorial was inspired by, and copied liberally from, Columbia's [ESP tutorial](https://esp.cs.columbia.edu/tutorials/isca2024/docker).



