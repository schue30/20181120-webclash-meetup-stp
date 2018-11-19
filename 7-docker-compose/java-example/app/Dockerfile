FROM openjdk:8-slim

WORKDIR /app
ADD application.jar /app/application.jar
USER 1000
ENTRYPOINT ["java", "-server", "-jar", "/app/application.jar"]
