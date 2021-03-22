---
title: "Risk"
description: "Covering the Risk API."
lead: "Covers use of the Risk API."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu: 
  docs:
    parent: "api"
weight: 150
toc: true
---

# Overview

In this section we cover the `Risk Model` Api. The `Risk Model` api covers the following endpoints.

| Endpoint | Method | Description |
| --- | --- | -- |
| `/riskmodel/{id}` | `GET` | Get the latest version specific for a given risk model definition |
| `/riskmodel/{id}/version/{versionId}` | `GET` | Get a specific risk model version |
| `/riskmodel` | `GET` | List all registered risk models |
| `/riskmodel/{id}/activate` | `PUT` | Activate a deactivated risk model |
| `/riskmodel/{id}/deactivate` | `PUT` | Deactivate an active risk model |
| `/riskmodel` | `POST` | Create a new risk model |
| `/riskmodel/{id}` | `POST` | Update an existing risk model, this creates a new risk model version instance |

A risk model entry looks like the following

```json
{
  "id": "1",
  "name": {
    "en-US": "Default Risk Model"
  },
  "description": {
    "en-US": "Default Risk Model Description"
  },
  "createdOn": "2021-03-22T08:51:59.238Z",
  "createdBy": "1",
  "updatedOn": "2021-03-22T08:51:59.238Z",
  "updatedBy": "1",
  "active": true,
  "numberOfDimensions": 1,
  "numberOfScales": 2,
  "dimensions": [{
    "id": 1,
    "name": { "en-US": "Seriousness" },
    "description": { "en-US": "Seriousness description" },
    "scales": [{
      "value": 1,
      "name": { "en-US": "Not serious" },
      "description": { "en-US": "Not serious description" }
    }, {
      "value": 2,
      "name": { "en-US": "Very serious" },
      "description": { "en-US": "Very serious description" }
    }]
  }]
}
```