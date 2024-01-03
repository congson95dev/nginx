# Use the official Python base image
FROM python:3.9-slim

# Copy the application code to the working directory
COPY . ./fastapi_simple_app_2/
WORKDIR /fastapi_simple_app_2

# Install the project dependencies
RUN pip install --no-cache-dir -r fastapi_simple_app_2/requirements.txt