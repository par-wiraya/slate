# Errors

> HTTP Response for when exceeding bulk limit

```javascript
// header
HTTP/1.1 400 Bad Request
Content-Type: application/json; charset=utf-8
Date: Wed, 26 Apr 2017 08:20:47 GMT

// body
{
  "bulkItemLimitExceeded": true
}
```

Normally errors are identified by an error HTTP status code.

> HTTP Response for partially successful bulk request

```javascript
// header
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Date: Wed, 26 Apr 2017 08:20:47 GMT

// body
{
  "id":    
  [
    "49584134327499146337076065330038012842683545324179423234",
    null
  ]
  "error": true,
  "failures":
  {
    "12345":
    {
      "retry": true
    }
  }
}
```

A bulk request can be partially successful.


