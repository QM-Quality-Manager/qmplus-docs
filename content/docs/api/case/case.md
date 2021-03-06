---
title: "Case"
description: "Covering the case handling API."
lead: "Covers use of case API."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu: 
  docs:
    parent: "case"
weight: 130
toc: true
---

## Overview

In this chapter we will look at how we can retrieve the case, modify it and also retrieve history. Its important to understand that a case is associated with an entity and workflow. The types of entities supported are.

| Entity | Description |
| --- | --- |
| `MESSAGE` | A case attached to a specific registered message |
| `ACTION` | A case representing an Action to resolve one or more messages |
| `DOCUMENT` | A case representing a document and its associated process |
| `AUDIT` | A case representing an audit process of one or more documents |
| `HEARING` | A case representing a hearing process for a given document |

Cases are created when they are associated to an entity. For each entity there is a Case associated with it. The case represents the organisational work around handling the event.

## Retriving a case

In this first use case we will show how to retrieve a case for a specific message.

```bash
curl -X GET "https://app.qmplus.com/api/case/message/1" -H  "accept: application/json" -H  "auth-impersonate-tenant-id: 104" -H  "auth-impersonate-user-id: 1000001" -H  "auth-tenant-id: 0" -H  "auth-token: 1698b0b29c7d4bd7f1f6a73d60552e4c"
```

```json
{
  "entityId": "1",
  "entityTypeId": "MESSAGE_ENTITY",
  "workflowId": "5",
  "caseStatusId": "1",
  "createdOn": 1614289485234,
  "createdBy": "1",
  "updatedOn": 1614289485234,
  "updatedBy": "1",
  "version": "1",
  "fields": [{
    "date": 1614289485234,
    "fieldId": "1",
    "users": [{
      "departmentId": "1",
      "userId": "1"
    }],
    "values": ["somevalue"]
  }],
  "tasks": [{
    "doneDate": 1614289485234,
    "dueDate": 1614289485234,
    "participants": [{
      "departmentId": "1",
      "doneDate": 1614289485234,
      "state": "PENDING",
      "times": [{
        "doneDate": 1614289485234,
        "timeUsage": 0
      }],
      "type": "CASE_HANDLER",
      "userId": "1"
    }],
    "plannedHours": 0,
    "plannedStartDate": 1614289485234,
    "registeredOn": 1614289485234,
    "state": "PENDING",
    "transitionId": "1",
    "updatedBy": "1",
    "updatedOn": 1614289485234
  }],
  "attachments": [{
    "contentType": "image/png",
    "id": "111111",
    "name": "acme.png",
    "size": "131312321"
  }],
  "references": [{
    "entityId": "10000",
    "entityType": "MESSAGE_ENTITY",
    "triggerOnTransactionIds": [],
    "type": "CLOSE_ON"
  }],
  "followers": ["1", "2"]
}
```

Lets look at the top level object returned in detail and what each field means. Then we look at the embedded documents in details

### Case Description

| Field | Description |
| --- | --- |
| `entityId` | The id of the entity the case is associated with |
| `entityTypeId` | One of the following values `MESSAGE_ENTITY, ACTION_ENTITY, HEARING_ENTITY, AUDIT_ENTITY, DOCUMENT_ENTITY` |
| `workflowId` | The id of the associated workflow id |
| `caseStatusId` | The id of the current case status in the above workflow the case is in |
| `createdOn` | The date the case was created |
| `createdBy` | The id of the user who created the case |
| `updatedOn` | The date the case was last updated |
| `updatedBy` | The id of the user who last updated the case |
| `version` | The current version of the case |
| `fields` | Fields associated with this case, the fields come from dialogs associated with the transitions and this field stores the case specific values |
| `tasks` | The list of tasks associated with the task, these are generated from the fields in dialogs when we transition from one state to another |
| `attachments` | Any files attached to the case |
| `references` | These are references from this case to other entities, depending on the reference type an action can be triggered |
| `followers` | List of user ids that follow the case and will be notified by changes |

### Field Description

A field represents a value that comes from a dialog field that was triggered by a transition. This could be for example a text field for a description or a selected current case worker.

| Field | Description |
| --- | --- |
| `fieldId` | The id of the field in a workflow dialog that this entry is attached to |
| `date` | The date the field was created |
| `values` | A list of values stored for the field |
| `componentValues` | A list of component values stored for the field |
| `users` | A list of user ids associated with this field, could be the users assigned to a task for example |

#### Field Component Description 

Some field types have components associated with them. One example is when creating an action the field have several components such as a DUE_DATE.





### Task Description

### Attachment Description

### Refrence Description

