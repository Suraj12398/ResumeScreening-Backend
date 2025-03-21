# Use an official Java runtime as a base image
FROM openjdk:17-jdk-slim

# Set the working directory inside the container
WORKDIR /app

# Copy only the Gradle wrapper separately first to ensure permissions
COPY gradlew .
COPY gradle/wrapper gradle/wrapper

# Grant execute permission to the Gradle wrapper
RUN chmod +x gradlew

# Copy the rest of the application files
COPY . .

# Build the application
RUN ./gradlew build

# Expose the port your application runs on
EXPOSE 8080

# Start the application
CMD ["./gradlew", "bootRun"]

