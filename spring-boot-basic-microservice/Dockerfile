# Use an official OpenJDK runtime as a base image
FROM openjdk:17-jdk-slim

# Define build-time arguments
ARG SPRING_BOOT_APP_NAME
ARG SPRING_BOOT_PORT

# Set environment variables for use inside the container
ENV SPRING_BOOT_APP_NAME=${SPRING_BOOT_APP_NAME}
ENV SPRING_BOOT_PORT=${SPRING_BOOT_PORT}

# Set the working directory in the container
WORKDIR /spring-boot-microservice-currency-conversion-service

# Copy the Spring Boot JAR file into the container
COPY target/spring-boot-microservice-currency-conversion-service-0.0.1-SNAPSHOT.jar ${SPRING_BOOT_APP_NAME}-0.0.1-SNAPSHOT.jar

# Expose the port for the Spring Boot application
EXPOSE ${SPRING_BOOT_PORT}

# Run the Spring Boot application
ENTRYPOINT ["java", "-jar", "${SPRING_BOOT_APP_NAME}-0.0.1-SNAPSHOT.jar"]