# Stage 1: Build the WAR
FROM maven:3.9.6-eclipse-temurin-17 AS builder

WORKDIR /app

COPY settings.xml /root/.m2/settings.xml
COPY pom.xml .
COPY src ./src

RUN mvn clean install

# Stage 2: Deploy to Tomcat
FROM tomcat:9-jdk11

RUN rm -rf /usr/local/tomcat/webapps/*

COPY --from=builder /app/target/surya-latest.war \
     /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]