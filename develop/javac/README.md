## Java Development

Build a docker image for Java Development.

### Build

    docker build -t develop/javac .

### Usage

#### Compile Java source files

    docker run -v $(pwd):/work -w /work develop/javac -cp "bin:lib/*" -d bin -sourcepath src Main.java
