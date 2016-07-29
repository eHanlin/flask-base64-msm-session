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

## LICENSE

The MIT License (MIT)

Copyright (c) 2016 eHanlin Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

