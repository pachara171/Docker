# Use an official debian sid as a parent image
FROM debian:sid

# add PSU repository
RUN echo "deb http://mirrors.psu.ac.th/debian/ sid " \
         "main contrib non-free" > /etc/apt/sources.list

# Update and Upgrade system then install python3
RUN apt update && apt upgrade -y
RUN apt install -y python3 python3-dev python3-pip

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip3 install --trusted-host pypi.python.org -r requirements.txt

# Make port 8000 available to the world outside this container
EXPOSE 8000

# Define environment variable, change it to your infomation
ENV WORLD Docker
ENV STUDENT_ID "6310110297"
ENV NAME "Pachara Yuanlea"

# Run app.py when the container launches
CMD ["python3", "app.py"]
