FROM python:3.5.2

# Set the default directory where CMD will execute
WORKDIR /app

# install requirements
# this way when you build you won't need to install again
# and since COPY is cached we don't need to wait
COPY app/requirements.txt /app/requirements.txt
RUN pip3 install --upgrade -r /app/requirements.txt

# Copy the application folder inside the container
COPY app /app

# Run command specified in the k8s.yaml file
CMD ["bokeh", "serve", "bokeh_app.py", "--port", "8080"]
