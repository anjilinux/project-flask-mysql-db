# Use an official Python runtime as a parent image
FROM python:2.7-slim

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Define environment variable
ENV MYSQL_USER python
ENV MYSQL_PASS python
ENV MYSQL_HOST mysql
ENV MYSQL_DB sample

# Run app.py when the container launches
CMD ["python", "app.py"]
