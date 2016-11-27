
# Copyright 2016 Jiglesgom

FROM jiglesgom/javaruntime:7
MAINTAINER jiglesgom <jiglesgom@gmail.com>

RUN apt-get update &&\
  apt-get -y install ca-certificates &&\
  wget -q https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.8/bin/apache-tomcat-8.5.8.tar.gz.md5 &&\
  wget -q https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.8/bin/apache-tomcat-8.5.8.tar.gz &&\
  md5sum -c apache-tomcat-8.5.8.tar.gz.md5 &&\
  tar xzf apache-tomcat-8.5.8.tar.gz &&\
  rm /apache-tomcat-*.tar.gz* &&\
  mv /apache-tomcat-8.5.8 /tomcat &&\
  cd /tomcat/webapps &&\
  rm -Rf ROOT docs examples host-manager manager
  
EXPOSE 8080

ENTRYPOINT ["/tomcat/bin/catalina.sh"]

CMD ["run"]