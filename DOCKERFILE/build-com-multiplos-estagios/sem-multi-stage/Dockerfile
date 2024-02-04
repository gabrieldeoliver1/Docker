FROM maven:3.8.6-eclipse-temurin-11-alpine

COPY my-app /app

WORKDIR /app

RUN mvn package

ENTRYPOINT [ "java" ]

CMD ["-cp", "target/my-app-1.0-SNAPSHOT.jar", "com.mycompany.app.App"]