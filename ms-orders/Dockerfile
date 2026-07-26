FROM eclipse-temurin:17-jre-alpine
WORKDIR /opt
EXPOSE 9091
COPY target/*.jar /opt/app.jar
ENTRYPOINT exec java $JAVA_OPTS -jar app.jar