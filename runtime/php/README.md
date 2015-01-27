## PHP Runtime

Build a docker image for PHP Runtime.

### Build

    docker build -t runtime/php .

### Usage

#### Execute PHP file

    docker run -v $(pwd):/work -w /work runtime/php info.php

#### Start a testing web server

    docker run -v $(pwd):/work -w /work runtime/php -S 0.0.0.0:8000
