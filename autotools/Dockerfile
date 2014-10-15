FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install autoconf automake libtool gnulib gettext pkg-config
RUN apt-get clean && rm /var/lib/apt/lists/* -rf
