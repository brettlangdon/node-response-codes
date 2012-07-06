## Response Codes ##


### Install
```
npm install response-codes
```

### Usage
```
var http = require('http');
require('response-codes');

http.createServer( function(req,res){
  switch(req.url){
  case '/':
    res.OK('thanks');
    break;
  case '/private':
    res.UNAUTHORIZED('STAY AWAY!');
    break;
  default:
    res.NOTFOUND('nothing to see here, move along');
    break;
  }
}).listen(1337);

```

This module also works with web frameworks such as Express.

### Functions

Functions can be accessed by their name `res.OK('message');` as well as their status code `res[200]('message');`

  * `CONTINUE( message, headers )`
  * `SWITCHING_PROTOCOLS( message, headers )`
  * `OK( message, headers )`
  * `CREATED( message, headers )`
  * `ACCEPTED( message, headers )`
  * `NON_AUTHORITATIVE_INFORMATION( message, headers )`
  * `NO_CONTENT( message, headers )`
  * `RESET_CONTENT( message, headers )`
  * `PARTIAL_CONTENT( message, headers )`
  * `MULTITPLE_CHOICES( message, headers )`
  * `MOVED_PERMAMENTLY( message, headers )`
  * `FOUND( message, headers )`
  * `SEE_OTHER( message, headers )`
  * `NOT_MODIFIED( message, headers )`
  * `USE_PROXY( message, headers )`
  * `TEMPORARY_REDIRECT( message, headers )`
  * `BAD_REQUEST( message, headers )`
  * `UNAUTHORIZED( message, headers )`
  * `PAYMENT_REQUIRED( message, headers )`
  * `FORBIDDEN( message, headers )`
  * `NOT_FOUND( message, headers )`
  * `METHOD_NOT_ALLOWED( message, headers )`
  * `NOT_ACCEPTABLE( message, headers )`
  * `PROXY_AUTHENTICATION_REQUIRED( message, headers )`
  * `REQUEST_TIMEOUT( message, headers )`
  * `CONFLICT( message, headers )`
  * `GONE( message, headers )`
  * `LENGTH_REQUIRED( message, headers )`
  * `PRECONDITION_FAILED( message, headers )`
  * `REQUEST_ENTITY_TOO_LARGE( message, headers )`
  * `REQUEST_URI_TOO_LONG( message, headers )`
  * `UNSUPPORTED_MEDIA_TYPE( message, headers )`
  * `REQUESTED_RANGE_NOT_SATISFIABLE( message, headers )`
  * `EXPECTATION_FAILED( message, headers )`
  * `INTERNAL_SERVER_ERROR( message, headers )`
  * `NOT_IMPLEMENTED( message, headers )`
  * `BAD_GATEWAY( message, headers )`
  * `SERVICE_UNAVAILABLE( message, headers )`
  * `GATEWAY_TIMEOUT( message, headers )`
  * `HTTP_VERSION_NOT_SUPPORTED( message, headers )`