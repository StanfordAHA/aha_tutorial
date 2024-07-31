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

TODO: should we create a demo docker image instead??

Pull Image

```
docker pull stanfordaha/garnet:latest
```

Run Docker

```
docker run -it -d --name ${container_name} stanfordaha/garnet:latest bash
```

# Attribution

This tutorial was inspired by, and copied liberally from, Columbia's <a href=https://esp.cs.columbia.edu/tutorials/isca2024/docker/>ESP tutorial.</a>



