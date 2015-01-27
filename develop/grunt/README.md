## Grunt

Build a docker image for Grunt.

### Build

    docker build -t develop/grunt .

### Usage

#### Run the default task:

    docker run -v $(pwd):/work -w /work develop/grunt

#### Run the watch task daemon:

    docker run -d -v $(pwd):/work -w /work develop/grunt watch
