# Use an official Python 3 as a parent image
FROM python:3-slim

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Make port 8000 available to the world outside this container
EXPOSE 8000

# Define environment variable
ENV WORLD Docker
ENV STUDENT_ID "6310110297"
ENV NAME "PACHARA YUANLEA"

# Run app.py when the container launches
CMD ["python", "app.py"]