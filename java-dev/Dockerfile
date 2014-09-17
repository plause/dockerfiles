FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y openjdk-7-jdk ant maven
RUN apt-get clean && rm /var/lib/apt/lists/* -rf
