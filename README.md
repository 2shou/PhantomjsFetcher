# PhantomjsFetcher
A python web fetcher using phantomjs to mock browser

Before using
------------
1. install [phantomjs](http://phantomjs.org/download.html) and start it:

  $ phantomjs phantomjs_fetcher.js [port]

2. install tornado

  $ pip install tornado

Sample Code
-----------

```python
from tornado_fetcher import Fetcher

# create a fetcher
>>> fetcher=Fetcher(user_agent='phantomjs', phantomjs_proxy='http://localhost:12306', poolsize=10)
# fetch webpage from url
>>> fetcher.fetch(url)
# or execute a javascrpt after render end
>>> fetcher.fetch(url, js_script='setTimeout("window.scrollTo(0,100000)", 1000)')
```
