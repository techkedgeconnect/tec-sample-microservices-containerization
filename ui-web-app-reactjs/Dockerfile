# Use the official Node.js image as the base image
# This image includes Node.js runtime and npm (Node Package Manager)
FROM node:latest

# Add metadata to the image to identify the maintainer
LABEL email="techkedgeconnect@gmail.com"

# Set the working directory inside the container
WORKDIR /app

# Copy all files from the current directory on the host machine
# to the `/app` directory inside the container
COPY . .

# Run npm install to install all the dependencies listed in the package.json file
RUN npm install

# Expose port 8080 so that the application can be accessed from outside the container
EXPOSE 8080

# Specify the command to run when the container starts
# This runs `npm start` to start the application using the start script defined in package.json
CMD ["npm","start"]