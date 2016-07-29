flask-base64-msm-session
=======================================

This project is a session extension of flask. Using memcached server replace original session.

The data encoder use [https://github.com/eHanlin/memcached-session-manager/tree/1.8.3-base64](https://github.com/eHanlin/memcached-session-manager/tree/1.8.3-base64).

Your python project with java project is able to share session.

## Install

```sh
pip install flask-base64-msm-session
```

## Usage

You only need to set `session_interface`.

```py
from flask_base64_msm_session.session_processor import MemcachedSessionProcessor
from flask import Flask

app = Flask(__name__)
app.session_cookie_name = 'JSESSIONID'
app.session_interface = MemcachedSessionProcessor(['localhost:11211'])
```


