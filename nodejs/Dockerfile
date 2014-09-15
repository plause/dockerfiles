FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y apt-transport-https

ADD https://deb.nodesource.com/gpgkey/nodesource.gpg.key /tmp/nodesource.gpg.key
RUN apt-key add /tmp/nodesource.gpg.key && rm /tmp/nodesource.gpg.key -f
ADD etc/apt/sources.list.d/nodesource.list /etc/apt/sources.list.d/

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y nodejs
RUN apt-get clean && rm /var/lib/apt/lists/* -rf
