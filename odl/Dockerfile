############################################################
# Dockerfile to build OpenDaylight Lithium Controller
# Based on Ubuntu
############################################################

#Base image to use
FROM ubuntu

#File Author
MAINTAINER Luis Villatoro

#Update repository List
RUN apt-get update
RUN apt-get -y install wget

#Install JDK 7
RUN apt-get install -y openjdk-7-jdk

#Download and Install ODL

RUN mkdir opendaylight
RUN wget -q "https://nexus.opendaylight.org/content/repositories/opendaylight.release/org/opendaylight/integration/distribution-karaf/0.3.2-Lithium-SR2/distribution-karaf-0.3.2-Lithium-SR2.tar.gz"
RUN tar -xf distribution-karaf-0.3.2-Lithium-SR2.tar.gz -C opendaylight
RUN rm -rf distribution-karaf-0.3.2-Lithium-SR2.tar.gz

EXPOSE 162 179 1088 1790 1830 2400 2550 2551 2552 4189 4342 5005 5666 6633 6640 6653 7800 8000 8080 8101 8181 8383 120

WORKDIR /opendaylight
ENV JAVA_HOME /usr/lib/jvm/java-7-openjdk-amd64/bin/java
CMD ["./bin/karaf", "server"]
