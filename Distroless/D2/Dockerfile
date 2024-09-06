# Use an official Python base image to build the app
FROM python:3.9-slim AS build

# Set working directory
WORKDIR /app

# Copy the Python script
COPY app.py .

# Distroless base image for Python
FROM gcr.io/distroless/python3

# Copy the app from the build stage
COPY --from=build /app /app

# Set the working directory
WORKDIR /app

# Expose the port the app will run on
EXPOSE 8080

# Run the Python script
CMD ["app.py"]
