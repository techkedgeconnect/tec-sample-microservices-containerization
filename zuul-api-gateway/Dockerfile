# Stage 1: Build stage
# Use the official Maven image as the base for the build stage
# This image contains Maven and the necessary build tools for compiling a Java project
FROM maven as build

# Add metadata to the image, specifying the maintainer's email address
LABEL email=techkedgeconnect@gmail.com

# Set the working directory for the build stage inside the container
WORKDIR /app

# Copy all project files from the host machine's current directory
# to the /app directory in the container
COPY . .

# Run Maven to install dependencies and build the project
# This will compile the project and create the JAR file in the target directory
RUN mvn install

# Stage 2: Run stage
# Use a lightweight OpenJDK 17 image for the runtime environment
# This helps to reduce the size of the final Docker image since only the runtime environment is needed
FROM openjdk:17-jdk-slim

# Set the working directory inside the container for the runtime stage
WORKDIR /app

# Copy the compiled JAR file from the build stage to the runtime stage
# The JAR file is copied from /app/target in the build stage to the /app directory in this stage
COPY --from=build /app/target/zuul-0.0.1-SNAPSHOT.jar /app 

# Expose port 9999 to allow external systems to connect to the application running inside the container
EXPOSE 9999

# Specify the command to run the Java application when the container starts
CMD ["java", "-jar", "zuul-0.0.1-SNAPSHOT.jar"]

