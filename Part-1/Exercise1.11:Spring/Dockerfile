#
# Build stage
#
FROM maven:3.6.0-jdk-11-slim AS build
COPY src /home/app/src
COPY pom.xml /home/app
RUN mvn -f /home/app/pom.xml clean package

#
# Package stage
#
FROM openjdk:8

COPY . .

#RUN ./mvnw package

EXPOSE 8080

CMD ["java","-jar","./target/docker-example-1.1.3.jar"]