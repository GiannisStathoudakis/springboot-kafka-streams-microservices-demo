FROM eclipse-temurin:17-jre-alpine
WORKDIR /opt
EXPOSE 8080
COPY target/*.jar /opt/app.jar
ENTRYPOINT exec java $JAVA_OPTS -jar app.jar