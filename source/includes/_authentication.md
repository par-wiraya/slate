# Authentication

> HTTP Request

```javascript
// header
POST https://api.wiraya.ai/auth/Token/apikey HTTP/1.1
Content-Type: application/json; charset=utf-8

// body
{
  "key": "YOUR_API_KEY"
}
```

> HTTP Response

```javascript
// header
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Date: Wed, 26 Apr 2019 08:20:47 GMT

// body
{
  "authenticated": true,
  "token": "string",
  "tokenExpires": "2019-04-26T08:25:42.0418136Z"
}
```

The API uses tokens to authenticate requests. The token is acquired by calling the single endpoint that does not require such a token, and passing your API key to it. The returned response contains the token and its expiration date. Any future calls to the API needs to have this token passed in the header.

Each call to the WAI API needs to be secured with a token. It is acquired by calling the single endpoint that does not require such a token, and passing your API Key to it. Returned is a response that holds the token and its expiration date. Any future calls to the API needs to have this token passed in a header.

