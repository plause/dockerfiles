FROM ubuntu:trusty

RUN apt-get update && apt-get -y install nodejs nodejs-legacy && rm /var/lib/apt/lists/* -rf

ENTRYPOINT ["nodejs"]
