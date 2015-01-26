## GNU Build System

Build a docker image for the GNU Build System.

### Build

    docker build -t develop/autotools .

### Usage

#### Using autoconf:

    docker run -v $(pwd):/work develop/autotools autoreconf -if

#### Run configure script:

    docker run -v $(pwd):/work develop/autotools ./configure --prefix=/usr

#### Make dists:

    docker run -v $(pwd):/work develop/autotools make dist

#### Generate new PO file:

    docker run -v $(pwd):/work develop/autotools msginit -i po/example.pot -o po/zh_CN.po -l zh_CN.UTF-8
