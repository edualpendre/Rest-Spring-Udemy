FROM openjdk:15-jdk-slim
VOLUME /tpm
ADD target/restWithSpring-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8080
RUN bash -c 'touch /app.jar'
ENTRYPOINT ["java", "-Djava.security.eg=file:/dev/./urandom", "-jar", "/app.jar"]