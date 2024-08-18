# Use the official Python 3 image as the base image
# This includes the Python runtime and necessary libraries
FROM python:3

# Add metadata to the image, such as the maintainer's email address
LABEL email=techkedgeconnect@gmail.com

# Copy all files from the current directory on the host machine
# to the root directory inside the container
COPY . .

# Install the required Python packages, in this case, Flask and Flask-CORS
# These are essential dependencies for building and running the Flask web application
RUN pip install flask flask_cors

# Expose port 1003 so that the Flask application running inside the container
# can be accessed externally through this port
EXPOSE 1003

# Define the command to run when the container starts
CMD ["python", "index.py"]

