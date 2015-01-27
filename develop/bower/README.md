## Bower

Build a docker image for Bower.

### Build

    docker build -t develop/bower .

### Usage

#### Run the init process

    docker run -v $(pwd):/work -w /work develop/bower init --allow-root

#### Install and save your dependencies:

    docker run -v $(pwd):/work -w /work develop/bower install --allow-root --save jquery

#### Update all your dependencies:

    docker run -v $(pwd):/work -w /work develop/bower update --allow-root
