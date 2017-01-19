# Copyright 2016 Jiglesgom

FROM tschuss/java8:latest
MAINTAINER jiglesgom <jiglesgom@gmail.com>

#clonar eureka y lanzar el build
# RUN env GIT_SSL_NO_VERIFY=true git clone https://github.com/Tschuss/springboot_demo.git
RUN env GIT_SSL_NO_VERIFY=true git clone https://github.com/spring-cloud-samples/eureka.git
RUN cd eureka 

# Standard SSH port
EXPOSE 8761

# Default command
CMD ["mvn", "-X", "spring-boot:run"]
