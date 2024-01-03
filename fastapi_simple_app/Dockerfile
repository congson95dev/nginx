# Use the official Python base image
FROM python:3.9-slim

# Copy the application code to the working directory
COPY . ./fastapi_simple_app/
WORKDIR /fastapi_simple_app

# Install the project dependencies
RUN pip install --no-cache-dir -r requirements.txt