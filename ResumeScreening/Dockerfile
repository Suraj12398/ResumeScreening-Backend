# Use an official Java runtime as a base image
FROM openjdk:17-jdk-slim

# Set the working directory inside the container
WORKDIR /app

# Copy all project files into the container
COPY . .

# Grant execute permission to Gradle wrapper
RUN chmod +x gradlew

# Build the application
RUN ./gradlew build

# Expose the port your application runs on (update if needed)
EXPOSE 8080

# Start the application
CMD ["./gradlew", "bootRun"]

