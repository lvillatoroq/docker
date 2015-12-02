############################################################
# Dockerfile to build OpenDaylight Lithium Controller
# Based on Alpine Latest
############################################################

#Base image to use
FROM gliderlabs/alpine:latest

#File Author
MAINTAINER Luis Villatoro

#Install JDK 7
RUN apk add --update openjdk7-jre-base openssl unzip && rm -rf /var/cache/apk/*

#Download and Install ODL
RUN mkdir opendaylight
RUN wget -q "https://nexus.opendaylight.org/content/repositories/opendaylight.release/org/opendaylight/integration/distribution-karaf/0.3.2-Lithium-SR2/distribution-karaf-0.3.2-Lithium-SR2.zip" && \
	unzip distribution-karaf-0.3.2-Lithium-SR2.zip -d opendaylight && \
	rm -rf distribution-karaf-0.3.2-Lithium-SR2.zip

EXPOSE 162 179 1088 1790 1830 2400 2550 2551 2552 4189 4342 5005 5666 6633 6640 6653 7800 8000 8080 8101 8181 8383 120

ENTRYPOINT ["./opendaylight/distribution-karaf-0.3.2-Lithium-SR2/bin/karaf"]
CMD []
