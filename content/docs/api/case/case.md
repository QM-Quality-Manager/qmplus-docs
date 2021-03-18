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
    parent: "api"
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
curl -X GET "https://app.qmplus.com/api/case/message/1" -H  "accept: application/json" -H  "auth-impersonate-tenant-id: 104" -H  "auth-impersonate-user-id: 1000001" -H  "auth-tenant-id: 0" -H  "auth-token: TOKEN"
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
    "values": ["somevalue"],
    "componentValues": [{
      "type": "PLANNED_START_DATE",
      "values": [1614289485234]
    }, {
      "type": "PLANNED_HOURS",
      "values": [40.0]
    }, {
      "type": "DUE_DATE",
      "values": [1614289485234]
    }],
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

The types of components available are.

| Name | Description |
| --- | --- |
| `PLANNED_START_DATE` | The planned start date for this component |
| `PLANNED_HOURS` | The number of hours expected for the task |
| `DUE_DATE` | The date the task is due to be done |

These can be considered sub elements of a field in a dialog and can be present or not depending on the original settings for a field in a form.

### Task Description

A task represents an activity performed by one or more persons associated with the case.

#### Top Level Object

This represents the field at the top of a task object

```json
{
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
}
```

| Name | Description |
| --- | --- |
| `doneDate` | The date the task was completed |
| `dueDate` | The date the task was due to be completed |
| `participants` | A list of participants on the task|
| `plannedHours` | The number of planned hours the task will take |
| `plannedStartDate` | The date the task should be started, should always be before the due date |
| `registeredOn` | The date the task was created |
| `state` | The state of the task |
| `transitionId` | The id of the transition that triggered the task creation |
| `updatedBy` | The id of the user who last updated the task |
| `updatedOn` | The date the task was last updated |

The task state can be one of the following values.

| Name | Description |
| --- | --- |
| `PENDING` | The task is pending |
| `COMPLETE` | The task was completed |
| `INACTIVE` | The task is inactive |

#### Participant Object

The participants object represents the people associated with a task and what kind of participant type they have.

```json
This represents the field at the top of a task object

```json
{
  "departmentId": "1",
  "doneDate": 1614289485234,
  "state": "PENDING",
  "times": [{
    "doneDate": 1614289485234,
    "timeUsage": 0
  }],
  "type": "CASE_HANDLER",
  "userId": "1"
}
```

| Name | Description |
| --- | --- |
| `departmentId` | The department the case participant belongs to |
| `doneDate` | The done date for this case participants work on the task |
| `state` | The state of the case participants |
| `times` | A list of work times registered for the case participant for this task |
| `type` | The type of case participant | 
| `userId` | The id of the user |

The case participant `state` can be one of the following values.

| Name | Description |
| --- | --- |
| `PENDING` | The task is pending |
| `COMPLETE` | The task was completed |
| `INACTIVE` | The task is inactive |

The case participant `type` can be one of the following values.

| Name | Description |
| --- | --- |
| `CASE_HANDLER` | The case participant is a task case handler |
| `CASE_PARTICIPATOR` | The case particpant is a participant in the task |
| `CASE_APPROVER` | The case participant is an approver for the task |

The case participant `times` is a list of registered work done for for the particular task.

```json
{
  "doneDate": 1614289485234,
  "timeUsage": 0
}
```

| Name | Description |
| --- | --- |
| `doneDate` | The date this amount of work was performed |
| `timeUsage` | The time spend for this period of work |

### Attachment Description

A list of case attachments.

```json
{
  "contentType": "image/png",
  "id": "111111",
  "name": "acme.png",
  "size": "131312321"
}
```

| Name | Description |
| --- | --- |
| `contentType` | The MIME content type of the attachment |
| `id` | The id of the attachment (used to download the attachment) |
| `name` | The name of the file stored as an attachment |
| `size` | The size of the file stored as an attachment |

### Refrence Description

Contains references to the entities in the system. This allows you to link cases together to make it clear how they are related.

```json
{
  "entityId": "10000",
  "entityType": "MESSAGE_ENTITY",
  "triggerOnTransactionIds": [],
  "type": "CLOSE_ON"
}
```

| Name | Description |
| --- | --- |
| `entityId` | The id of the entity we are referencing (document id, message id, action id, etc.) |
| `entityType` | The entityType of the reference. It can be one of either [`MESSAGE_ENTITY`, `ACTION_ENTITY`, `DOCUMENT_ENTITY`, `HEARING_ENTITY`, `AUDIT_ENTITY`] |
| `triggerOnTransitionIds` | A list of transition ids that will trigger an action on the reference, such as auto closing the associated message for an action |
| `type` | The type of the reference |

The case reference `type` can be one of the following values.

| Name | Description |
| --- | --- |
| `REFERENCE` | Just a reference between entities |
| `CLOSE_ON` | Close the referenced entity if a listed transition happens |


