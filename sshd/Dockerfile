FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install openssh-server
RUN mkdir /var/run/sshd
RUN apt-get clean && rm /var/lib/apt/lists/* -rf

CMD ["/usr/sbin/sshd", "-D"]

EXPOSE 22
