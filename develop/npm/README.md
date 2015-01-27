## NodeJS Package Manager

Build a docker image for NPM.

### Build

    docker build -t develop/npm .

### Usage

#### Install Packages declared in package.json:

    docker run -v $(pwd):/work -w /work develop/npm install
