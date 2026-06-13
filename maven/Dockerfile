FROM maven:3.9.6-eclipse-temurin-17
WORKDIR /app
RUN mkdir -p /root/.m2
COPY settings.xml /root/.m2/settings.xml
COPY pom.xml .
COPY src ./src
RUN mvn clean install
RUN mvn clean package tomcat7:deploy