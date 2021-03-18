---
title: "Overview"
description: "Covering the tenant authentication API."
lead: "Covers use of tenant authentication API."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu: 
  docs:
    parent: "authentication"
weight: 100
toc: true
---

## Overview

The platform supports multiple authentication mechanisms and additional security protocols. A tenant can be configured to support one or more authentication mechanisms and even have separate authentication mechanisms for different parts of the organization (when you have daughter companies you wish to integrate into the platform but they exist with their own legacy authentication mechanisms).

## Tenant

This documentation covers the `tenant` authentication api calls. These are made up of the following endpoints.

| Endpoint | Description |
| --- | --- |
| `/authentication/tenant` | Validates if a tenant exists. If it does it returns an object with the details of the tenant and its available authentication mechanism |

### Request a tenant

We can check if a tenant exists by either it's `tenantId` or its `name`. Lets look at an example that queries by the tenant name.

```bash
curl -X POST "https://app.qmplus.com/api/authentication/tenant" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 1000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"name\": \"ACME\"}"
```

We `POST` the following document.

```json
{
  "name": "ACME"
}
```

A suscessfull call will return a document that looks something like the following example.

```json
{
  "id": "1",
  "status": true,
  "name": "ACME",
  "displayName": "A company that makes everything",
  "description": "From rocket skates to nuclear bombs, everything you need to hunt roadrunners",
  "mechanisms": ["LOCAL"]
}
```

If the tenant does not exist we will get an error document in its place.

```json
{
  "code": "VALIDATION",
  "message": "failed validation of incoming document",
  "errors": [{
    "code": "VALIDATION",
    "paths": ["name", "tenantId"],
    "message": "tenant not found"
  }]
}
```

Lets look at the successful result object returned.

| Field | Description |
| --- | --- |
| `id` | The unique identifier for the tenant |
| `status` | Signals that the tenant exists |
| `name` | The name of the tenant |
| `displayName` | The name displayed for the tenant in the login window |
| `description` | A description of the tenant |
| `mechanisms` | The available authentication mechanisms for this tenant | 

The mechanisms provided by the platform is.

| Type | Description |
| --- | --- |
| `ADFS` | Supports `ADFS` direct authentication using username and password |
| `LOCAL` | Supports `LOCAL` direct authentication using username and password |
| `LDAP` | Supports `LDAP` direct authentication using username and password |
| `AZURE` | Supports `AZURE` direct authentication using username and password |
| `SAML_SSO` | Supports `SAML_SSO` single signon authentication |
