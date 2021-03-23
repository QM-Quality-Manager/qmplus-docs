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
| `/api/authentication/local/password/reset/request` | Request a password reset |
| `/api/authentication/local/password/reset` | Validate if a user and password exists |
| `/api/authentication/password/validate` | Validate a new password |

### Request Password

```bash
curl -X POST "https://app.qmplus.com/api/authentication/local/password/reset/request" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"tenantId\": \"1\", \"username\": \"peter\" }"
```

We `POST` the following document.

```json
{
  "tenantId": "1",
  "username": "peter"
}
```

A suscessfull call will return a document that looks something like the following example.

```json
{
  "status": true,
}
```

and will trigger a password reset link to be sent to the matching users email address. This email wil contain a link in the following format.

```
https://app.qmplus.com?reset=true&tenantId=1&userId=1&token=SOMETOKEN
```

The link includes the following fields

| Field | Description |
| --- | --- |
| `reset` | Password reset |
| `tenantId` | The tenantId of the tenant we are going to reset |
| `userId` | The userId of the user who we are reseting the password for |
| `token` | The token generated to ensure the reset can only be done with this link |

### Validate a new Password

```bash
curl -X POST "https://app.qmplus.com/api/authentication/password/validate" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"tenantId\": \"1\",\"userId\": \"1\", \"password\": \"newpassword\" }"
```

We `POST` the following document.

```json
{
  "tenantId": "1",
  "userId": "1",
  "password": "newpassword"
}
```

A suscessfull call will return a document that looks something like the following example.

```json
{
  "status": true,
  "errors": []
}
```

An error will return a list of keys that can be resolved to error messages.

```json
{
  "status": false,
  "errors": ["TOLONG"]
}
```

### Reset the Password

Once you have received the token from the email.

```bash
curl -X POST "https://app.qmplus.com/api/authentication/local/password/reset" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"tenantId\": \"1\",\"username\": \"peter\", \"token\": \"TOKEN\", \"password\": \"newpassword\", \"confirmPassword\": \"newpassword\" }"
```

We `POST` the following document.

```json
{
  "tenantId": "1",
  "token": "TOKEN",
  "password": "newpassword",
  "confirmPassword": "newpassword"
}
```

A suscessfull call will return a document that looks something like the following example.

```json
{
  "status": true,
}
```

At this point the password has been validated.




