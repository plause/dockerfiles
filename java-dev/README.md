## Java Development

Build a docker image for Java Development.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/java-dev/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

The best practice of using this image is to build your own from it.
Here is an example dockerfile:

    FROM base/java-dev

    # mirror your account inside the image
    # same uid and same login name
    RUN useradd -m -u 1000 -s /bin/bash plause

    # switch to the new user
    USER plause

    # stay focus to the project
    WORKDIR /work

Build an image from the new dockerfile:

    docker build -t plause/java-dev .

and use it like these:

#### Build a project using Java Compiler:

    docker run --rm -v $(pwd):/work plause/java-dev javac -cp "bin:lib/*" -d bin -sourcepath src Main.java
