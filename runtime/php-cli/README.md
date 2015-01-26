## PHP Runtime

Build a docker image for PHP Runtime.

### Build

    docker build -t runtime/php-cli .

### Usage

#### Execute PHP file

    docker run -v $(pwd):/work -w /work runtime/php-cli info.php

#### Start a testing web server

    docker run -v $(pwd):/work -w /work runtime/php-cli -S 0.0.0.0:8000
