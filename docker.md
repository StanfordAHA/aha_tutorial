---
layout: default
permalink: /docker/
title:  Stanford AHA
---
# Using Docker to Run the AHA Flow

[Docker Overview](https://docs.docker.com/guides/docker-overview/)

# Install Docker

NOTE: prototype instructions from ESP tutorial can be found here:
<https://esp.cs.columbia.edu/tutorials/isca2024/docker>

```
sudo systemctl start docker
```

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
