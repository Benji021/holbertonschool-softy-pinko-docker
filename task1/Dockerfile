FROM ubuntu:latest

# Update and install the necessary packages
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y python3 python3-pip

# Installing Flask with pip3
RUN pip3 install flask

# Copy the Flask application into the image
COPY app.py /app/app.py

# Define working directory
WORKDIR /app

# Expose port 5000 to access Flask
EXPOSE 5000

# Command to start the Flask server
CMD ["python3", "app.py"]
