# Introduction

> Base URL

```javascript
https://api.wiraya.ai
```

The API aims to allow our clients to build technical integrations where their systems communicate directly with the Wiraya platform in order to use Wiraya Activation Intelligence.

The API consists of [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer) endpoints, meaning that the URL encodes the resource and the HTTP method defines the action.

As an API primarily intended for data ingress, there’s no implementation for DELETE operations.

The Content-Type of the requests to the API is defined to be application/json with the UTF-8 character set. The JSON standard (RFC4627) defines how certain primitive types such as strings, integers, floats, objects, and arrays are to be encoded, but complex types such as datetime has no literal syntax provided. To that end, this specification defines that in communicating with the API, dates are to be encoded according to the ISO 8601 standard: “2016-04-11T09:11:43Z” or “2016-04-11T09:11:43.573921Z”. Note that the trailing “Z” is the ISO8601 designation for UTC.

If you're missing some feature or have any questions, please let us know!