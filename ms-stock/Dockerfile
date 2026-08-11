FROM eclipse-temurin:17-jre-alpine
WORKDIR /opt
EXPOSE 8080
COPY target/*.jar /opt/app.jar
RUN addgroup --system javauser && adduser --system --group javauser && chown -R javauser:javauser /opt
USER javauser
ENTRYPOINT ["sh", "-c", "exec java $JAVA_OPTS -jar app.jar"]