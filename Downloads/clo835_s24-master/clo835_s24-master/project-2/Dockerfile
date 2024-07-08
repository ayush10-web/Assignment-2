# Use official Python Runtime as aa parent image
FROM python:latest

# Set the working directory to /app
WORKDIR /app

# Copy the app.py into the container at /app

COPY app.py /app

# Make port 3000 available to the outside worl
EXPOSE 3030

#Run the app.y when container launches
CMD ["python", "app.py"]

