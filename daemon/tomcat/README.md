## Apache Tomcat

Build a docker image for Apache Tomcat.

### Build

    docker build -t daemon/tomcat7 .

### Usage

#### Run a Web application:

    docker run -d -v $(pwd)/app.war:/var/lib/tomcat7/webapps/app.war daemon/tomcat7
