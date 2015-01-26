## NodeJS Development

Build a docker image for NodeJS Development.

### Build

    docker build -t develop/nodejs .

### Usage

#### Install Packages declared in package.json:

    docker run -it -v $(pwd):/work -w /work develop/nodejs install
