## Apache Ant

Build a docker image for Apache Ant.

### Build

    docker build -t develop/ant .

### Usage

#### Build your project

    docker run -v $(pwd):/work -w /work develop/ant -Dsome.property=some.value target1 target2
