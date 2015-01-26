FROM ubuntu:trusty

RUN apt-get update && apt-get -y install openjdk-7-jre-headless && rm /var/lib/apt/lists/* -rf

ENTRYPOINT ["java"]
