FROM openjdk:17-jdk-slim
WORKDIR /watchService
COPY . .
RUN ./gradlew build
CMD ["java", "-jar", "build/libs/watchService-0.0.1-SNAPSHOT.jar"]
EXPOSE 8080