Flask-Imagine-RackspaceAdapter
============

[![Author](https://img.shields.io/badge/author-Kronas-blue.svg)](https://github.com/kronas)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/kronas/Flask-Imagine/master/LICENSE)
[![Documentation Status](https://readthedocs.org/projects/flask-imagine/badge/?version=latest)](http://flask-imagine.readthedocs.org/en/latest/?badge=latest)

Rackspace Files adapter for [Flask-Imagine](https://github.com/FlaskGuys/Flask-Imagine) extension.

Installation
------
```
$ pip install Flask-Imagine-RackspaceAdapter
```

Configuration example
------
```
from flask import Flask
from flask.ext.imagine import Imagine
from flask.ext.imagine_rackspace_adapter import FlaskImagineRackspaceAdapter

app = Flask(__name__)

app.config['IMAGINE_ADAPTERS'] = {
    'rackspace': FlaskImagineRackspaceAdapter
}

app.config['IMAGINE_ADAPTER'] = {
    'name': 'rackspace',
    'region': 'your_region',
    'user_name': 'your_user_name',
    'api_key': 'your_api_key',
    'container_name': 'your_container_name'
}

# ... Another configuration options

# Init extension
imagine = Imagine(app)
#  or 
imagine = Imagine()
imagine.init_app(app)
```
