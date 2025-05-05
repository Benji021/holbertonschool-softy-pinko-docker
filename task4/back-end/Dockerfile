FROM ubuntu:latest

# Update packages
RUN apt-get update && apt-get upgrade -y

# Install Python 3 and pip3
RUN apt-get install -y python3 python3-pip

# Solve the “EXTERNALLY-MANAGED” problem
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask with pip3
RUN pip3 install flask flask-cors

# Define working directory
WORKDIR /app

# Copy api.py file to image
COPY api.py /app/api.py

# Expose port 5252
EXPOSE 5252

# Start Flask server
CMD ["python3", "/api.py"]
