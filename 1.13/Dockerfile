FROM openjdk:8 
RUN mkdir -p /usr/app
WORKDIR /usr/app
COPY spring-example-project . 
#WORKDIR /usr/app/spring-example-project
RUN ./mvnw package
CMD java -jar ./target/docker-example-1.1.3.jar
