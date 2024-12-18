# Use an official OpenJDK runtime as a base image
FROM openjdk:17-jdk-slim

# Set the working directory in the container
WORKDIR /spring-boot-basic-microservice/${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}

# Copy the Spring Boot JAR file into the container
COPY target/${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}-0.0.1-SNAPSHOT.jar ${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}-0.0.1-SNAPSHOT.jar

# Expose port 9090 for the Spring Boot application
EXPOSE ${SPRING_BOOT_CURRENCY_CONVERSION_PORT}

# Run the Spring Boot application
ENTRYPOINT ["java", "-jar", "${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}-0.0.1-SNAPSHOT.jar"]
