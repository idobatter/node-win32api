# NAME

node-win32api - Asynchronous, non-blocking win32api bindings for [node.js](https://github.com/joyent/node) .


# USAGE

Install with `npm install win32api`.

``` js
var win32con = require('win32con');
var win32api = require('win32api');
var MessageBoxA = win32api.new('user32', 'MessageBoxA', 'LPPL', 'L');
var result = MessageBoxA.call(win32api.hWnd, 'Hello, Win32API', 'test message',
  win32con.MB_ICONINFORMATION | win32con.MB_OK);
win32api.print(result);
var MessageBoxW = win32api.new('user32', 'MessageBoxW', 'LPPL', 'L');
var result = MessageBoxW.call(win32api.hWnd, 'from utf8string', 'auto convert',
  win32con.MB_ICONINFORMATION | win32con.MB_OK);
win32api.print(result);
```


# FEATURES

* So much implements.
* Implement accessors getter, setter and caller.
* npm


# API

See the [API documentation](https://github.com/idobatter/node-win32api/wiki) in the wiki.


# BUILDING

This project uses VC++ 2008 Express (or later) and Python 2.6 (or later) .
(When using Python 2.5, it needs [multiprocessing 2.5 back port](http://pypi.python.org/pypi/multiprocessing/) .)

Bulding also requires node-gyp to be installed. You can do this with npm:

    npm install -g node-gyp

To obtain and build the bindings:

    git clone git://github.com/idobatter/node-win32api.git
    cd node-win32api
    node-gyp configure
    node-gyp build

You can also use [`npm`](https://github.com/isaacs/npm) to download and install them:

    npm install win32api


# TESTS

[mocha](https://github.com/visionmedia/mocha) is required to run unit tests.

    npm install -g mocha
    nmake /a test


# CONTRIBUTORS

* [idobatter](https://github.com/idobatter)


# ACKNOWLEDGEMENTS

Inspired [WIN32API](http://www.ruby-doc.org/stdlib/libdoc/win32api/rdoc/)


# LICENSE

`node-win32api` is [BSD licensed](https://github.com/idobatter/node-win32api/raw/master/LICENSE).
