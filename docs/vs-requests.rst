Compatibility with requests
***************************

Although we try our best to mimic the requests API, some functionality is not easy to implement and left out.
Here are a list of known incompatibilities:

- files API are slightly different, but more error-proof.
- retries are not supported yet, tracked in [#24](https://github.com/lexiforest/curl_cffi/issues/24)
- redirect history are not supported, tracked in [#82](https://github.com/lexiforest/curl_cffi/issues/82)
- empty-domains cookies may lost during redirects, tracked in [#55](https://github.com/lexiforest/curl_cffi/issues/55)
- response object can not be pickled.
- The ``requests`` proxies dict is supported, but we prefer ``proxy=...``, unless you really use different proxies for http and https.
- You can use use transports/adapters, instead, you can use ``curl_cffi`` as adapter for ``reuqests``.


Transports and Adapters
=======================

``curl_cffi`` is deeply coupled with ``libcurl-impersonate``. Unlike ``requests`` or ``httpx``,
There is no way to use a different networking library or mount different adapters.

Alternatively, you can use ``curl-cffi`` as a requests adapter via `curl-adapter <https://github.com/el1s7/curl-adapter>`_.
In this way, you get the full functionality of requests.
