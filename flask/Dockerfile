# Use an official Python runtime as a parent image
FROM python:2.7-slim

#Use an official MySQL runtime as a parent image
#FROM mysql:5.7

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Make port 5000 available to the world outside this container
EXPOSE 5000

# Define environment variable
ENV NAME World
ENV MYSQL_USER python
ENV MYSQL_PASS python
ENV MYSQL_HOST flask-db
ENV MYSQL_DB sample

# Run app.py when the container launches
CMD ["python", "app.py"]
