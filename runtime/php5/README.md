## PHP5 Runtime

Build a docker image for PHP5 Runtime.

### Build

    docker build -t runtime/php5 .

### Usage

#### Execute PHP file

    docker run -v $(pwd):/work -w /work runtime/php5 info.php

#### Start a testing web server

    docker run -v $(pwd):/work -w /work runtime/php5 -S 0.0.0.0:8000
