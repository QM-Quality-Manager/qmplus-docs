---
title: "Calendar"
description: "Covering the Calendar and Activity API."
lead: "Covers use of the Calendar and Activity API."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu: 
  docs:
    parent: "api"
weight: 130
toc: true
---

## Overview

This section covers operating on `Calendar` objects and their associated `Activities` in qmplus. A tenant can have multiple calender entries.

The relevant swagger information is located at.

[Swagger Calendar API](https://app.qmplus.com/swagger-ui/index.html?contextPath=&requestServerName=app.qmplus.com#/calendars)

## Calendar Operations

The calendar is the top level object used for handling activities. There can be one or more Calendar objects for a tenant and they can be placed on different departments and can be inherited by child departments.

### Create a Calendar

Lets create a couple of departments, and look at what it means. First create a simple department level Calendar.

Lets start by creating payload object defining a new Calendar with no activites.

```json
{
    "activities": [],
    "departmentId": "1",
    "name": {
        "en_US": "Service Routines"
    },
    "description": {
        "en_US": "Contains all service activities for the ACME department"
    },
    "references": [],
    "tags": [],
    "visibility": "DEPARTMENT"
}
```

You can execute this using the following curl statement. You'll need to provide your own parameters.

| Field | Description | Example Value |
| --- | ---- | ---- |
| `TENANT_USER_ID` | The id of the user we are going to execute the operation under. | `10000001` |
| `TENANT_ID` | The id of the tenant we are executing the operation against. | `104` |
| `TOKEN` | The authentication token to execute the operation under. | `1698aabbbcff4bd7f1f6affd60552e4c` |

```bash
curl 'https://app.qmplus.com/api/calendar' \
  -H 'auth-impersonate-user-id: TENANT_USER_ID' \
  -H 'Content-Type: application/json' \
  -H 'auth-impersonate-tenant-id: TENANT_ID' \
  -H 'auth-tenant-id: TENANT_ID' \
  -H 'auth-token: TOKEN' \
  --data-raw '{"activities":[],"departmentId":"1","name":{"en_US":"Service Routines"},"description":{"en_US":"Contains all service activities for the ACME department"},"references":[],"tags":[],"visibility":"DEPARTMENT"}' \
  --compressed
```

### Updating a Calendar entry

Given a calendar entry with id `1` we are going to update the name, description, tags, add a reference and an activity. Lets start by creating the update object.

```json
{
    "activities": ["1"],
    "departmentId": "1",
    "name": {
        "en_US": "Service Routines 2"
    },
    "description": {
        "en_US": "Contains all service activities for the ACME department 2"
    },
    "references": [{
        "id": "1",
        "type": "FILE",
        "location": "INTERNAL",
        "reference": {
            "id": "1",
            "version": 0
        }
    }],
    "tags": ["service"],
    "visibility": "DEPARTMENT"
}
```

The reference object contains a reference to a `FILE` document that is `INTERNAL` with the `id` of `1` and `version` of `0`.

The curl operation would look something like this.

```bash
curl 'https://app.qmplus.com/api/calendar/1' \
  -H 'auth-impersonate-user-id: TENANT_USER_ID' \
  -H 'Content-Type: application/json' \
  -H 'auth-impersonate-tenant-id: TENANT_ID' \
  -H 'auth-tenant-id: TENANT_ID' \
  -H 'auth-token: TOKEN' \
  --data-raw '{"activities":["1"],"departmentId":"1","name":{"en_US":"Service Routines 2"},"description":{"en_US":"Contains all service activities for the ACME department 2"},"references":[{"id":"1","type":"FILE","location":"INTERNAL","reference":{"id":"1","version":0}}],"tags":["service"],"visibility":"DEPARTMENT"}' \
  --compressed
```
