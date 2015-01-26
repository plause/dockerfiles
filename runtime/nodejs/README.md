## NodeJS Runtime

Build a docker image for NodeJS Runtime.

### Build

    docker build -t runtime/nodejs .

### Usage

#### Run JavaScript file:

    docker run -v $(pwd):/work -w /work runtime/nodejs server.js
