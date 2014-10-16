## Java Development

Build a docker image for Java Development.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/java-dev/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

The best practice of using this image is to build your own from it.
Here is an example dockerfile:

    FROM plause/java-dev

    # mirror your account inside the image
    # same uid and same login name
    RUN useradd -m -u 1000 -s /bin/bash plause

    # save maven downloads
    VOLUME ["/home/plause/.m2"]

    # switch to the new user
    USER plause

    # stay focus to the project
    WORKDIR /project

Build an image from the new dockerfile:

    docker build -t project/java-dev .

and use it like these:

#### Build a project using Apache Ant:

    docker run --rm -v $(pwd):/project project/java-dev ant

#### Build a project using Apache Maven:

    docker run --rm -v $(pwd):/project project/java-dev mvn test
