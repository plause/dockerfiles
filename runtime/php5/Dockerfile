FROM ubuntu:trusty

RUN apt-get update && apt-get -y install php5-cli && rm /var/lib/apt/lists/* -rf

ENTRYPOINT ["php"]
