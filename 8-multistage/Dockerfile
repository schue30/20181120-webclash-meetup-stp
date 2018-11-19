FROM openjdk:8-slim as builder

WORKDIR /build
COPY example-app/* /build/
RUN ./gradlew clean assemble && \
    mv build/libs/*.jar build/libs/application.jar


FROM openjdk:8-jre-slim

WORKDIR /app
COPY --from=builder /build/build/libs/application.jar /app
USER 1000

ENTRYPOINT ["java", "-server", "-jar", "/app/application.jar"]
