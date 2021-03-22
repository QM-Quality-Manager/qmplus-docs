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
| `/riskmodel/{id}/version` | `GET` | Get the risk model versions |
| `/riskmodel/{id}/version/{versionId}` | `GET` | Get a specific risk model version |
| `/riskmodel` | `GET` | List all registered risk models |
| `/riskmodel` | `POST` | Create a new risk model |
| `/riskmodel/{id}` | `POST` | Update an existing risk model, this creates a new risk model version instance |
| `/riskmodel/{id}/activate` | `PUT` | Activate a deactivated risk model |
| `/riskmodel/{id}/deactivate` | `PUT` | Deactivate an active risk model |

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

The dimensions and scales make up a risk model. The dimensions and scales make up a matrix that is used to calculate a risk.

| Dimension 1 | Dimension 2 | Dimension 3|
| --- | --- | --- |
| Scale 1-1 | Scale 2-1 | Scale 3-1 |
| Scale 1-2 | Scale 2-2 | Scale 3-2 |
| Scale 1-3 | Scale 2-3 | Scale 3-3 |
| Scale 1-4 | Scale 2-4 | Scale 3-4 |
| Scale 1-5 | Scale 2-5 | Scale 3-5 |

A user can create a category group that is tied to a risk model. A category group added to a form will render the selected categories as risk calculation entries based on the risk model attached.

Each `column` contains values where the columns have a value from `1 - numberOfScales`. Each dimension is then multipled to create the final risk score.

For example the user has selected

```
Scale 1-2 * Scale 2-3 * Scale 3-4
```

Gets translated to

```
2 * 3 * 4 = 24
```

Where a higher value is considered a higher risk.

## Create a risk model

Lets look at how we can create a risk model. This involves the following endpoint.

| Endpoint | Method | Description |
| --- | --- | --- |
| `/api/riskmodel` | `POST` | Create a new risk model entry |

An example curl operation would look something like this.

```bash
curl -X POST "https://app.qmplus.com/api/riskmodel" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 1000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{\"name\":{\"en-US\":\"Default Risk Model\"},\"description\":{\"en-US\":\"Default Risk Model Description\"},\"active\":true,\"numberOfDimensions\":1,\"numberOfScales\":2,\"dimensions\":[{\"id\":1,\"name\":{\"en-US\":\"Seriousness\"},\"description\":{\"en-US\":\"Seriousness description\"},\"scales\":[{\"value\":1,\"name\":{\"en-US\":\"Not serious\"},\"description\":{\"en-US\":\"Not serious description\"}},{\"value\":2,\"name\":{\"en-US\":\"Very serious\"},\"description\":{\"en-US\":\"Very serious description\"}}]}]}"
```

We `POST` the following document.

```json
{
  "name": {
    "en-US": "Default Risk Model"
  },
  "description": {
    "en-US": "Default Risk Model Description"
  },
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

This will create a risk model with `1 dimension` where each dimension has `2 scale entries`.

## Update an existing risk model

Lets how we can update an existing risk model. This uses the following endpoint.

| Endpoint | Method | Description |
| --- | --- | --- |
| `/riskmodel/{id}` | `POST` | Update an existing risk model, this creates a new risk model version instance |

```bash
curl -X POST "https://app.qmplus.com/api/riskmodel/1" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 1000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{\"name\":{\"en-US\":\"Default Risk Model\"},\"description\":{\"en-US\":\"Default Risk Model Description\"},\"active\":true,\"numberOfDimensions\":1,\"numberOfScales\":2,\"dimensions\":[{\"id\":1,\"name\":{\"en-US\":\"Seriousness\"},\"description\":{\"en-US\":\"Seriousness description\"},\"scales\":[{\"value\":1,\"name\":{\"en-US\":\"Not serious\"},\"description\":{\"en-US\":\"Not serious description\"}},{\"value\":2,\"name\":{\"en-US\":\"Very serious\"},\"description\":{\"en-US\":\"Very serious description\"}}]}]}"
```

We `POST` the following document.

```json
{
  "name": {
    "en-US": "Default Risk Model"
  },
  "description": {
    "en-US": "Default Risk Model Description"
  },
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

This will update an existing risk model with `1 dimension` where each dimension has `2 scale entries`.

## List the available risk models

To list the available risk models use the following endpoint.

| Endpoint | Method | Description |
| --- | --- | -- |
| `/riskmodel` | `GET` | List all registered risk models |

You cam pass the following parameters.

| Name | Description |
| --- | --- |
| `includeFields` | Fields of the resulting object you want to include |
| `excludeFields` | Fields of the resulting object you want to exclude |
| `skip` | Number of entries to skip |
| `limit` | Limit of entries to return |
| `active` | Filter either on active/non active or include both |

This will return a list of the latest version of each risk model. An example result of a risk model entry would look something like.

```json
{
  "id": "1",
  "version": 1,
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

## Fetch the latest version of specific risk model

To retireve a specific risk model use the following endpoint.

| Endpoint | Method | Description |
| --- | --- | -- |
| `/riskmodel/{id}` | `GET` | Get the latest version specific for a given risk model definition |

This will retrieve a risk model document that looks something like the document below.

```json
{
  "id": "1",
  "version": 1,
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

## Fetch all versions for a specific risk model

To retireve a specific risk models versions ordred by version number in descending order use the following endpoint.

| Endpoint | Method | Description |
| --- | --- | -- |
| `/riskmodel/{id}/version` | `GET` | Get the risk model versions |
definition |

This will return an array of all the versions of a risk model.

```json
{
  "id": "1",
  "riskModelId": "2",
  "version": 1,
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

## Fetch a specific version of a risk model

To retireve a specific risk model version use the following endpoint.

| Endpoint | Method | Description |
| --- | --- | -- |
| `/riskmodel/{id}/version/{versionId}` | `GET` | Get a specific risk model version |

This will return the object for the specific risk model version.

```json
{
  "id": "1",
  "riskModelId": "2",
  "version": 1,
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

## Activate a risk model

Use the following endpoint to activate a risk model

| Endpoint | Method | Description |
| --- | --- | -- |
| `/riskmodel/{id}/activate` | `PUT` | Activate a deactivated risk model |

## Deactivate a risk model

Use the following endpoint to deactivate a risk model

| Endpoint | Method | Description |
| --- | --- | -- |
| `/riskmodel/{id}/deactivate` | `PUT` | Deactivate an active risk model |















