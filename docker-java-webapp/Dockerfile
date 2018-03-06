FROM maven:3-jdk-8

LABEL maintainer "Alexander Malic <alexander.malic@maastrichtuniversity.nl>"
LABEL maintainer "Pedro Hernandez <p.hernandezserrano@maastrichtuniversity.nl>"

ENV APP_DIR /app

WORKDIR $APP_DIR

COPY . .

RUN mvn clean build

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "target/gs-serving-web-content-0.1.0.jar"]