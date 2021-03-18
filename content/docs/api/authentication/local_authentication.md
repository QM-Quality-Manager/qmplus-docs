---
title: "Local Authentication"
description: "Covering the local authentication API."
lead: "Covers use of local authentication API."
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

## Local Authentication

In this section we look at local authentication and how to proceed with getting authenticated using a locally defined user and password.

| Endpoint | Description |
| --- | --- |
| `/api/authentication/local` | Validate if a user and password exists |

### 1. Perform a user and password validation

Lets attempt to authenticate a local username and password. The user is not configured with two-factor authentication enabled.

```bash
curl -X POST "https://app.qmplus.com/api/authentication/local" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 1000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"tenantId\": \"1\", \"username\": \"peter\", \"password\": \"somepassword\" }"
```

We `POST` the following document.

```json
{
  "tenantId": "1",
  "username": "peter",
  "password": "somepassword"
}
```

A suscessfull call will return a document that looks something like the following example.

```json
{
  "status": true,
  "twoFactorRequired": false,
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

##### Note
> If `twoFactorRequired` is set to true we will need to perform a two-factor authentication step before we can move onto the setting the `userType` step.

### 2. Sets the userType for the session

Given the above user type.

```json
{
  "departmentId": "1",
  "userTypeId": "1"
}
```

We call the following endpoint to set the `userTypeId`.

```bash
curl -X POST "https://app.qmplus.com/api/authentication/usertype" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 1000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"departmentId\": \"1\", \"userTypeId\": \"1\" }"
```

We `POST` the following document.

```json
{
  "departmentId": "1",
  "userTypeId": "1"
}
```

Give a successful call we receive a simple ok response.

```json
{
  "status": true
}
```





