Development and contributing
==============

This page documents how to compile curl-impersonate and curl-cffi from source. If binary
package is not available on your platform, you may refer to this page for some inspirations.

First, you need to check if there are libcurl-impersonate binaries for you platform. If
so, you can simply download and install them.

For now, a pre-compiled `libcurl-impersonate` is downloaded from github and built
into a bdist wheel, which is a binary package format used by PyPI. However, the
right way is to download curl and curl-impersonate sources on our side and compile
them all together.

macOS

To install the local editable build:

.. code-block:: shell

    # This is for using the libcurl-impersonate built by GitHub actions

    sudo mkdir /Users/runner
    sudo chmod 777 /Users/runner

    # Dependencies

    brew install libidn2 zstd

    # Then install

    pip install -e .[test]
    pip install -e .[dev]

Contributing
------------

When opening PR, please do not use the ``main`` branch in your fork, otherwise I cannot add my modification,
such as unittests.
