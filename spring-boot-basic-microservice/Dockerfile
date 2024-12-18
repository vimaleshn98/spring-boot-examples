# Use an official OpenJDK runtime as a base image
FROM openjdk:17-jdk-slim

# Define build-time arguments
ARG SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME
ARG SPRING_BOOT_CURRENCY_CONVERSION_PORT

# Set environment variables for use inside the container
ENV SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME=${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}
ENV SPRING_BOOT_CURRENCY_CONVERSION_PORT=${SPRING_BOOT_CURRENCY_CONVERSION_PORT}

# Set the working directory in the container
WORKDIR /spring-boot-basic-microservice/${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}

# Check the working directory again after changing it
RUN echo "Working directory after WORKDIR: $(pwd)"

# Copy the Spring Boot JAR file into the container
COPY target/${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}-0.0.1-SNAPSHOT.jar ${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}-0.0.1-SNAPSHOT.jar

# Expose port 9090 for the Spring Boot application
EXPOSE ${SPRING_BOOT_CURRENCY_CONVERSION_PORT}

# Run the Spring Boot application
ENTRYPOINT ["java", "-jar", "${SPRING_BOOT_APP_CURRENCY_CONVERSION_NAME}-0.0.1-SNAPSHOT.jar"]