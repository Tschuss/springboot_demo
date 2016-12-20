# Copyright 2016 Jiglesgom


FROM ubuntu:trusty
MAINTAINER jiglesgom <jiglesgom@gmail.com>

# Install Oracle Java 8
ENV JAVA_VER 8
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle
RUN echo 'deb http://ppa.launchpad.net/webupd8team/java/ubuntu trusty main' >> /etc/apt/sources.list 
RUN echo 'deb-src http://ppa.launchpad.net/webupd8team/java/ubuntu trusty main' >> /etc/apt/sources.list 
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys C2518248EEA14886 
RUN apt-get update 
RUN echo oracle-java${JAVA_VER}-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections 
RUN apt-get install -y --force-yes --no-install-recommends oracle-java${JAVA_VER}-installer oracle-java${JAVA_VER}-set-default 

#install maven    
RUN apt-get install -y --force-yes --no-install-recommends python-software-properties 
#RUN add-apt-repository ppa:webupd8team/java 
RUN apt-get update 
RUN apt-get install -y --force-yes --no-install-recommends maven
RUN apt-get install -y --force-yes --no-install-recommends git

#install gradle
RUN apt-get install -y --force-yes --no-install-recommends curl
RUN apt-get install -y --force-yes --no-install-recommends zip
RUN apt-get install -y --force-yes --no-install-recommends unzip
RUN curl -s https://get.sdkman.io | bash
#RUN source ".sdkman/bin/sdkman-init.sh"
#RUN sdk install gradle 3.2.1

#RUN apt-get clean 
#RUN rm -rf /var/lib/apt/lists 
#RUN rm -rf /var/cache/oracle-jdk${JAVA_VER}-installer    

#clonar eureka y lanzar el build
#RUN pwd
#RUN env GIT_SSL_NO_VERIFY=true git clone https://github.com/spring-cloud-samples/eureka.git
#RUN cd eureka &&\ mvn -X spring-boot:run 

    
# Standard SSH port
EXPOSE 22 8761

# Default command
CMD ["/usr/sbin/sshd", "-D"]