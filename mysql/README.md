## MySQL Client

Build a docker image for MySQL Client.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/mysql/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

#### Connect to the remote server:

    docker run --rm -it plause/mysql mysql --user root --port 3306 --host mysql-server --password
