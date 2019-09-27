# Contacts

The Contact entity represents an individual, an end user to communicate with at some point. Each contact stores the information that is relevant on an individual level such as phone number, gender, age, location as well as interests and any other metadata applicable. Providing this information helps WAI to draw behavioral conclusions based on this data.

## Send a contact

> HTTP Request for sending a contact

```javascript
PUT https://api.wiraya.ai/api/Contact/12345 HTTP/1.1
Authorization: Bearer [YOUR_TOKEN]
Content-Type: application/json

{
  "personal":
  {
    "phoneNumber":"46704134561",
    "givenName": "John",
    "surName": "Doe",
    "title": "Mr",
    "gender": "Male",
    "birthDate": "1980-01-01"
  },
  "general":
  {
    "city": "Testershire",
    "county": "Dorset",
    "country": "UK",
    "timeOfRegistration": "2018-03-30T16:43:11Z",
    "postCode": "DT11 0PS",
    "accountStatus": "active",
    "forgotPasswdTimes": 7,
    "latestClientDetailUpdate": "2018-04-11T11:21:43Z",
    "nrLogins": 6,
    "latestLogin": "2018-05-07T19:22:11Z"
  }
}
```

> HTTP Response for sending a contact

```javascript
HTTP/1.1 200 OK
Date: Wed, 26 Apr 2017 08:28:52 GMT

{
  "id": ["49593967912456823050646721704338680985139835900719529986"],
  "error": false,
  "failures": {}
}
```

`PUT https://api.wiraya.ai/api/Contact/[contactID]`

Sends a contact. The `contactID` represents your contact id which you will refer back to when additional data, such as events and metrics, should be posted to that contact. Let it be an identifier of the customer that is not resolvable to an individual by a 3rd part.

**Contact Request Model**

`javascript
{
  personal { ... }
  general { ... }
}
`

In the "personal" section, put user information (PII) that needs to be cleared at end of project (e.g. data privacy laws).

In the "general" section, put user information that is generic enough to not identify a specific individual.

