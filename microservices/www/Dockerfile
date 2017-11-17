# Set the base image to Ubuntu
FROM ubuntu:16.04

# Update the sources list
RUN apt-get -y update

# Install basic applications
RUN apt-get install -y tar git curl nano wget dialog net-tools build-essential

# Install Python and Basic Python Tools
RUN apt-get install -y python python-dev python-distribute python-pip

RUN pip install bokeh
RUN pip --version

# Copy the application folder inside the container
ADD /app /app

# Expose ports
EXPOSE 5006

# Set the default directory where CMD will execute
WORKDIR /app

# Set the default command to execute
# when creating a new container
# i.e. using CherryPy to serve the application
CMD ["bokeh", "serve", "bokeh_app.py"]
