## Java Runtime

Build a docker image for Java Runtime.

### Build

    docker build -t runtime/java .

### Usage

#### Execute a main class

    docker run --rm -v $(pwd)/classes:/classpath runtime/java -cp /classpath test.App hello

#### Execute a jar file

    docker run --rm -v $(pwd)/test-app.jar:/tmp/app.jar runtime/java -jar /tmp/app.jar hello
