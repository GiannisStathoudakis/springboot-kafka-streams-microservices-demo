FROM eclipse-temurin:17-jre-alpine
RUN apk update && apk upgrade --no-cache
WORKDIR /opt
EXPOSE 9091
COPY target/*.jar /opt/app.jar
RUN addgroup -S javauser && adduser -S javauser -G javauser && chown -R javauser:javauser /opt
USER javauser
ENTRYPOINT ["sh", "-c", "exec java $JAVA_OPTS -jar app.jar"]