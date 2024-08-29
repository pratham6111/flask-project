FROM docker.io/ubuntu:latest
WORKDIR /app
MAINTAINER prathameshmisal@gmail.com
# Update and install dependencies
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    python3-venv

# Copy the requirements file
COPY requirements.txt .

# Create a virtual environment and install Python dependencies
RUN python3 -m venv venv && \
    . venv/bin/activate && \
    pip install --upgrade pip && \
    pip install -r requirements.txt

# Copy the rest of the application code
COPY . .

# Expose the port the app will run on
EXPOSE 5000

# Set environment variable for Flask
ENV FLASK_APP=app.py

# Command to run the application
CMD ["venv/bin/python", "app.py"]

