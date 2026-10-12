# Use the latest official Ubuntu image as the base
FROM ubuntu:latest

# Update the APT package list
RUN apt-get update

# Upgrade all currently installed software packages automatically
RUN apt-get upgrade -y

# Install Python3 and pip3, skipping user input with -y
RUN apt-get install -y python3 python3-pip

# Fix externally managed environment error for pip packages on newer Ubuntu versions
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install the Flask web framework using pip3
RUN pip3 install flask

# Set the working directory inside the container to /app
WORKDIR /app

# Copy the local api.py script into the container's /app directory
COPY ./api.py /app/api.py

# Command to run the Flask application when the container starts
CMD ["python3", "api.py"]
