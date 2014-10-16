## NodeJS Development

Build a docker image for NodeJS Development.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/nodejs-dev/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

The best practice of using this image is to build your own from it.
Here is an example dockerfile:

    FROM plause/nodejs-dev

    # mirror your account inside the image
    # same uid and same login name
    RUN useradd -m -u 1000 -s /bin/bash plause

    # save npm caches, optional
    VOLUME ["/home/plause/.npm"]

    # switch to the new user
    USER plause

    # stay focus to the project
    WORKDIR /project

Build an image from the new dockerfile:

    docker build -t project/nodejs-dev .

and use it like these:

#### Install Packages declared in package.json:

    docker run --rm -it -v $(pwd):/project project/nodejs-dev npm install

#### Download browser components using bower:

    docker run --rm -it -v $(pwd):/project project/nodejs-dev bower install

#### Start a web server (grunt):

    docker run -d -p 9000 -v $(pwd):/project project/nodejs-dev grunt serve

#### Watch project file changes (grunt):

    docker run -d -v $(pwd):/project project/nodejs-dev grunt watch

#### Start a web server (gulp):

    docker run -d -p 9000 -v $(pwd):/project project/nodejs-dev gulp serve

#### Watch project file changes (gulp):

    docker run -d -v $(pwd):/project project/nodejs-dev gulp watch

#### Run tests:

    docker run --rm -v $(pwd):/project project/nodejs-dev karma start test.conf.js
