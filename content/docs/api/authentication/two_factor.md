---
title: "Two-factor"
description: "Covering the two factor authentication API."
lead: "Covers use of two facto authentication API."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu: 
  docs:
    parent: "authentication"
weight: 130
toc: true
---

## Two-factor Authentication

This section is an overview of how to perform a two-factor authentication step. For some `username/password` mechanisms the organization can set a two-factor authentication code requirement for the authentication process. This code can be delivered by multiple different means. For the current version of the platform this code is provdied by an email to the user.

| Endpoint | Description |
| --- | --- |
| `/authentication/twofactor` | Validate a two-factor code |

### Two-factor validation

A call to the `username/password` authentication mechanism returned an object that has the two factor requirement enabled which triggered an email to the user. This email included the two-factor code `61345` that is required to perform the second step.

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

Lets break down the returned document.

| Field | Description |
| --- | --- |
| `status` | Signals that the tenant exists |
| `twoFactorRequired` | If set to true we must perform a two-factor authentication step to logon |
| `departmentAndUserTypes` | A list of the users UserTypes with information |

The `departmentAndUserTypes` is a list of documents that have the following structure.

| Field | Description |
| --- | --- |
| `departmentId` | The id of the departmentId |
| `departmentName` | The name of the department |
| `userTypeId` | The userTypeId |
| `userTypeName` | The names by locale of the userType |

Given a successful authentication, we need to set the users userType and department so the platform can render the right view for the user.

