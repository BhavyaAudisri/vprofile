FROM maven:3.9.6-eclipse-temurin-17
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean install
RUN mkdir -p /root/.m2
COPY settings.xml /root/.m2/settings.xml