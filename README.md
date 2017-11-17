# python-bokeh

A simple python app using the `bokeh` library which runs on the `www` subdomain.

# Quickstart Instructions

```sh
$ hasura quickstart hasura/base-python-bokeh
$ cd base-python-bokeh
$ git add . && git commit -m "Initial Commit"
$ git push hasura master
```

Now, your app will be running at `https://www.YOUR-CLUSTER-NAME.hasura-app.io` (replace `YOUR-CLUSTER-NAME` with the name of your cluster). To get the name of your cluster

```sh
$ hasura cluster status
```

# Local development

Every time you push, your code will get deployed on a public URL. However, for faster iteration you should locally test your changes. To test your changes locally:

* Follow the instructions [here](http://bokeh.pydata.org/en/0.11.1/docs/user_guide/quickstart.html) to install `bokeh` on your local machine.

```sh
$ cd microservices/www/app
# Make your changes to the bokeh_app.py file
$ bokeh serve bokeh_app.py
```
