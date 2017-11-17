# Set the base image to Ubuntu
FROM ubuntu:16.04

# Update the sources list
RUN apt-get -y update

# Install basic applications
RUN apt-get install -y tar git curl nano wget dialog net-tools build-essential

# Install Python and Basic Python Tools
RUN apt-get install -y python python-dev python-distribute python-pip

RUN pip install bokeh

# Copy the application folder inside the container
ADD /app /app

# Set the default directory where CMD will execute
WORKDIR /app

# Run command specified in the k8s.yaml file
CMD ["bokeh", "serve", "bokeh_app.py", "--port", "8080"]
