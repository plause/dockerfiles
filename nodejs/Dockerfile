FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y wget apt-transport-https

RUN wget -qO- https://deb.nodesource.com/gpgkey/nodesource.gpg.key | apt-key add -

ADD etc/apt/sources.list.d/nodesource.list /etc/apt/sources.list.d/

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y nodejs
RUN apt-get clean && rm /var/lib/apt/lists/* -rf
