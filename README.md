# ftybr-add-to-req [![Build Status](https://secure.travis-ci.org/connrs/node-ftybr-add-to-req.png?branch=master)](http://travis-ci.org/connrs/node-ftybr-add-to-req)

To create your middleware object:

    var addToReq = require('ftybr-add-to-req');

Once you've instantiated it, you may add this middleware to your ftybr router:

    router.registerMiddleware(addToReq('someData', ['win']));

This middleware will create a req.data object containing the parsed data from any GET query string, POST form data and or POST JSON data. The POST data will overwrite any GET data.
