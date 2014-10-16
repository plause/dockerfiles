## Apache Tomcat

Build a docker image for Apache Tomcat.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/tomcat/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

#### Run a Web application:

    docker run -d -p 8080 -v $(pwd)/app.war:/var/lib/tomcat7/webapps/app.war
