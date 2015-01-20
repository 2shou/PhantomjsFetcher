# PhantomjsFetcher
A python web fetcher using phantomjs to mock browser

Before using
------------
1. install [phantomjs](http://phantomjs.org/download.html) and start with:

  `$ phantomjs phantomjs_fetcher.js [port]`

2. install tornado:

  `$ pip install tornado`

Sample Code
-----------

```python
from tornado_fetcher import Fetcher

# create a fetcher
>>> fetcher=Fetcher(
  user_agent='phantomjs', # user agent
  phantomjs_proxy='http://localhost:12306', # phantomjs url
  pool_size=10, # max httpclient num
  async=False
  )
# fetch html after rendering javascript from url
>>> fetcher.fetch(url)
# or execute additional javascript after rendering end
>>> fetcher.fetch(url, js_script='setTimeout("window.scrollTo(0,100000)", 1000)')
```

Reference
---------

[pyspider](https://github.com/binux/pyspider)
