# Use an official OpenJDK runtime as a base image
FROM openjdk:17-jdk-slim

# Set the working directory in the container
WORKDIR /spring-boot-2-rest-service-swagger

# Copy the Spring Boot JAR file into the container
COPY target/spring-boot-2-rest-service-swagger-0.0.1-SNAPSHOT.jar spring-boot-2-rest-service-swagger-0.0.1-SNAPSHOT.jar

# Expose port 9090 for the Spring Boot application
EXPOSE 9090

# Run the Spring Boot application
ENTRYPOINT ["java", "-jar", "spring-boot-2-rest-service-swagger-0.0.1-SNAPSHOT.jar"]
