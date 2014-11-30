FROM plause/java

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y tomcat7

ENV CATALINA_BASE /var/lib/tomcat7

RUN mkdir $CATALINA_BASE/temp && chown tomcat7:tomcat7 $CATALINA_BASE/temp
RUN apt-get clean && rm /var/lib/apt/lists/* -rf

USER tomcat7

EXPOSE 8080

WORKDIR /usr/share/tomcat7

CMD ["bin/catalina.sh", "run"]
