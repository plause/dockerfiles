## NodeJS Runtime

Build a docker image for NodeJS Runtime.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/nodejs/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

#### Install Packages:

    docker run --rm -v $(pwd):/app plause/nodejs npm install

#### Run JavaScript file:

    docker run --rm -p 3000 -v $(pwd):/app plause/nodejs node server.js
