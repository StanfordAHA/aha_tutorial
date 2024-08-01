---
layout: default
permalink: /docker/
title:  Stanford AHA
---
# Using Docker to Run the AHA Flow

[Docker Overview](https://docs.docker.com/guides/docker-overview/)

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

<i>TODO: should we create a demo docker image instead??</i>

The Docker image for this tutorial is available on DockerHub:
<a href=https://hub.docker.com/r/stanfordaha/garnet/>stanfordaha/garnet</a>
The image for the tutorial is `stanfordaha/garnet:latest` (about 6-8 GB in size).

Download the Docker image by running the following command (on Windows 10 you should run it in the PowerShell).
```
docker pull stanfordaha/garnet:latest
```
You may need to add login credentials to be able to pull. In that case you can add your credentials by running the following. A prompt will ask for your password as well.
```
docker login -u <your-dockerhub-username>
```
---BOOKMARK---

Run Docker

```
docker run -it -d --name ${container_name} stanfordaha/garnet:latest bash
```

## Attribution

This tutorial was inspired by, and copied liberally from, Columbia's <a href=https://esp.cs.columbia.edu/tutorials/isca2024/docker/>ESP tutorial.</a>



