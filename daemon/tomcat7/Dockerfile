FROM runtime/java

RUN apt-get update && apt-get -y install tomcat7 && rm /var/lib/apt/lists/* -rf

ENV CATALINA_BASE /var/lib/tomcat7
ENV CATALINA_TMPDIR /tmp

USER tomcat7

EXPOSE 8080

WORKDIR /usr/share/tomcat7

ENTRYPOINT [""]

CMD ["bin/catalina.sh", "run"]
