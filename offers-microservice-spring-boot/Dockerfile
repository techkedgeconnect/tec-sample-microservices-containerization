# Stage 1: Build stage
# Use the official Maven image as the base for the build stage
# This image includes Maven and the necessary tools for building a Java project
FROM maven as build

# Add metadata to the image with an email label
LABEL email=techkedgeconnect@gmail.com

# Set the working directory for the build stage inside the container
WORKDIR /app

# Copy all the source files and Maven configuration files from the current directory 
# on the host machine to the `/app` directory inside the container
COPY . .

# Run Maven to install dependencies and build the project
# This will generate a JAR file in the target directory
RUN mvn install

# Stage 2: Run stage
# Use a smaller OpenJDK image for running the application
# This helps in keeping the final image size smaller as this stage does not need Maven tools
FROM openjdk:17-jdk-slim

# Set the working directory for the run stage inside the container
WORKDIR /app

# Copy the built JAR file from the first stage (build stage) into the run stage
# This extracts the JAR file from `/app/target` in the build stage and places it in `/app` of the current stage
COPY --from=build /app/target/offers-0.0.1-SNAPSHOT.jar /app 

# Expose port 1001 to allow external access to the application running inside the container
EXPOSE 1001

# Specify the command to run the Java application when the container starts
CMD ["java", "-jar", "offers-0.0.1-SNAPSHOT.jar"]
