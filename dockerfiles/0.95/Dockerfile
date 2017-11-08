FROM openjdk:8u131-jre-alpine

WORKDIR /opt/tribe
ADD tarfile/tribestream-0.95.tar.gz .
EXPOSE 8080
CMD ["tribestream-0.95/bin/catalina.sh", "run"]