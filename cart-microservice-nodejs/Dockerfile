# Use the official Node.js 22 image as the base image
FROM node:22

# Add metadata to the image, specifically an email label
LABEL email=techkedgeconnect@gmail.com

# Set the working directory for the application inside the container
WORKDIR /app

# Copy all files from the current directory on the host machine 
# to the `/app` directory in the container
COPY . .

# Expose port 1004 so that the application inside the container 
# can be accessed through this port from the outside
EXPOSE 1004

# Specify the command to run when the container starts
CMD ["node", "index.js"]