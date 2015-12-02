############################################################
# Dockerfile to build OpenDaylight Helium Controller
# Based on Alpine Latest
############################################################

#Base image to use
FROM gliderlabs/alpine:latest

#File Author
MAINTAINER Luis Villatoro

#Install JDK 7
RUN apk add --update openjdk7-jre-base openssl unzip 

#Download and Install ODL

RUN mkdir opendaylight
RUN wget -q "https://nexus.opendaylight.org/content/groups/public/org/opendaylight/integration/distribution-karaf/0.2.4-Helium-SR4/distribution-karaf-0.2.4-Helium-SR4.zip" && \
	unzip distribution-karaf-0.2.4-Helium-SR4.zip -d opendaylight && \
	rm -rf distribution-karaf-0.2.4-Helium-SR4.zip

EXPOSE 162 179 1088 1790 1830 2400 2550 2551 2552 4189 4342 5005 5666 6633 6640 6653 7800 8000 8080 8101 8181 8383 120

ENTRYPOINT ["./opendaylight/distribution-karaf-0.2.4-Helium-SR4/bin/karaf"]
CMD []
