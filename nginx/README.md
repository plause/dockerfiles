## Nginx

Build a docker image for Nginx.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/nginx/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

#### Serve current folder:

    docker run --rm -p 80 -v $(pwd):/usr/share/nginx/html plause/nginx
