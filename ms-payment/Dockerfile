FROM gcr.io/distroless/java17-debian12:nonroot
WORKDIR /app
COPY target/*.jar app.jar
COPY grafana-opentelemetry-java.jar agent.jar
EXPOSE 8080
ENTRYPOINT ["java", "-javaagent:/app/agent.jar", "-javaagent:/app/pyroscope.jar", "-jar", "/app/app.jar"]