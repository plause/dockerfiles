FROM ubuntu:trusty

RUN apt-get update && apt-get -y install openjdk-7-jdk && rm /var/lib/apt/lists/* -rf

ENTRYPOINT ["javac"]
