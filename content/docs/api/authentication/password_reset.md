---
title: "Password Reet"
description: "Covering the password reset API."
lead: "Covers use of password reset API."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu: 
  docs:
    parent: "authentication"
weight: 150
toc: true
---

## Password Reset

This section covers the reset password functionality. This is only available for the local authentication mechanism as all other mechanisms are handled by external systems where reseting a users password is outside the reach of the platform.

| Endpoint | Description |
| --- | --- |
| `/authentication/local/password/reset/request` | Request a password reset |
| `/authentication/local/password/reset` | Validate if a user and password exists |

### Request Password

### Reset the Password

```bash
curl -X POST "https://app.qmplus.com/api/authentication/twofactor" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 1000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"code\": \"61345\", \"username\": \"peter\" }"
```

We `POST` the following document.

```json
{
  "code": "61345",
  "username": "peter"
}
```

A suscessfull call will return a document that looks something like the following example.

```json
{
  "status": true,
  "departmentAndUserTypes": [{
    "departmentId": "1",
    "departmentName": "ACME HQ",
    "userTypeId": "1",
    "userTypeName": {
      "en-US": "CEO"
    }
  }]
}
```
