## Composer

Build a docker image for Composer.

### Build

    docker build -t develop/composer .

### Usage

#### Install PHP packages

    docker run -v $(pwd):/work -w /work develop/composer require --ignore-platform-reqs PHP_PKG
