FROM openjdk:8-jre-alpine
WORKDIR /home/alpine
RUN apk update && apk add wget
ADD https://www.apache.org/dyn/closer.cgi?filename=/activemq/5.16.2/apache-activemq-5.16.2-bin.tar.gz&action=download amq.tar.gz
RUN tar -xvf amq.tar.gz --directory=/opt/
EXPOSE 8161 61616 5672 61613 1833
CMD ["/bin/sh","/opt/apache-activemq-5.16.2/bin/activemq","console"]
