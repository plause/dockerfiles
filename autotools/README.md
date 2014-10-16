## GNU Build System

Build a docker image for the GNU Build System.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/autotools/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

The best practice of using this image is to build your own from it.
Here is an example dockerfile:

    FROM plause/autotools

    # mirror your account inside the image
    # same uid and same login name
    RUN useradd -m -u 1000 -s /bin/bash plause

    # switch to the new user
    USER plause

    # stay focus to the project
    WORKDIR /project

Build an image from the new dockerfile:

    docker build -t project/clang-dev .

and use it like these:

#### Using autoconf:

    docker run --rm -v $(pwd):/project project/clang-dev autoreconf -if

#### Run configure script:

    docker run --rm -v $(pwd):/project project/clang-dev ./configure --prefix=/usr

#### Make dists:

    docker run --rm -v $(pwd):/project project/clang-dev make dist

#### Generate new PO file:

    docker run --rm -v $(pwd):/project project/clang-dev msginit -i po/example.pot -o po/zh_CN.po -l zh_CN.UTF-8
