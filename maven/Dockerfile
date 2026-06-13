FROM maven:3.9.6-eclipse-temurin-17
WORKDIR /app
RUN mkdir -p /root/.m2
COPY settings.xml /root/.m2/settings.xml
COPY pom.xml .
COPY src ./src
RUN sed -i 's/localhost/vprofile-mysql/g' src/main/resources/application.properties && \
    sed -i 's/3306/3306/g' src/main/resources/application.properties
RUN mvn clean install
RUN mvn clean package tomcat7:deploy