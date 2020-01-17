FROM openjdk:8 as build-stage
RUN mkdir -p /usr/app
WORKDIR /usr/app
COPY spring-example-project . 
RUN ./mvnw package
CMD java -jar ./target/docker-example-1.1.3.jar

FROM alpine:latest
RUN apk --no-cache add openjdk8-jre-base && mkdir -p /usr/app && adduser -D app && chown -R app:app /usr/app/
COPY --from=build-stage /usr/app/target /usr/app/target 
CMD java -jar /usr/app/target/docker-example-1.1.3.jar
