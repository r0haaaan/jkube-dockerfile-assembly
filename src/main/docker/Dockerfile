FROM alpine:latest
ARG JAR_FILE
ARG ASSEMBLY_PATH

RUN mkdir /application
COPY /${JAR_FILE} /application

ADD /${ASSEMBLY_PATH}/target/classes/hello/HelloWorld.class HelloWorld.class
RUN apk --update add openjdk8-jre
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/application/hello-world-0.1.0.jar"]
