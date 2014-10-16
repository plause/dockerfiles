## Java Runtime

Build a docker image for Java Runtime.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/java/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

#### Execute a main class

    docker run --rm -v $(pwd)/classes:/classpath plause/java java -cp /classpath test.App hello

#### Execute a jar file

    docker run --rm -v $(pwd)/test-app.jar:/tmp/app.jar plause/java java -jar /tmp/app.jar hello
