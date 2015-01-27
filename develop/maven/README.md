## Apache Maven

Build a docker image for Apache Maven.

### Build

    docker build -t develop/maven .

### Usage

#### Run tests

    docker run -v $(pwd):/work -w /work develop/maven test

#### Build packages

    docker run -v $(pwd):/work -w /work develop/maven package

#### Run a Jetty server for testing the web application

    docker run -v $(pwd):/work -w /work develop/maven jetty:run
