---
title: "Transition"
description: "Covering the transition handling API."
lead: "Covers use of transition API."
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

In this section we will cover performing transitions for a case using the `API`.

## Transitioning Between states with no Dialog

In this example we will show to trigger a transition for a specific message going from one state to another where there is no dialog associated with the transition. Lets say if you for example are modeling a `Kanban` style process where you can freely move a case between states.

Give that we have a message of `entityTypeId : MESSAGE_ENTITY` and with id `1` that is in the `open` case status with id `1` to the status `closed` with case status id `2`.

```json
{
  "transitionId": "1",
  "dialog": null
}
```

We trigger this with the following curl operation.

```bash
curl -X POST "https://app.qmplus.com/api/case/message/1/transition" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 1000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"dialog\": null, \"transitionId\": \"string\"}"
```

## Transitioning between states with a Dialog that contains all options

In this example we are going to perform a transition for a case using an attached dialog that contains all the possible fields for simplicities sake. Lets look at a dialog object from a workflow with all fields enabled.

```json
{
  "id": "2",
  "active": true,
  "name": {
    "no-NB": "Dialog"
  },
  "description": {
    "no-NB": ""
  },
  "fields": [
    {
      "id": "2",
      "name": {
        "no-NB": "textfield"
      },
      "active": true,
      "fieldType": "TEXTFIELD",
      "position": 0,
      "fieldComponents": []
    },
    {
      "id": "3",
      "name": {
        "no-NB": "textarea"
      },
      "active": true,
      "fieldType": "TEXTAREA",
      "position": 1,
      "fieldComponents": []
    },
    {
      "id": "4",
      "name": {
        "no-NB": "number"
      },
      "active": true,
      "fieldType": "NUMBER",
      "position": 2,
      "required": true,
      "fieldComponents": []
    },
    {
      "id": "5",
      "name": {
        "no-NB": "date"
      },
      "active": true,
      "fieldType": "DATE",
      "position": 3,
      "fieldComponents": []
    },
    {
      "id": "6",
      "name": {
        "en-GB": "Perform Task",
        "no-NB": "perform_task"
      },
      "active": true,
      "fieldType": "PERFORM_TASK",
      "position": 4,
      "fieldComponents": []
    },
    {
      "id": "7",
      "name": {
        "en-GB": "Action name",
        "no-NB": "action_name"
      },
      "active": true,
      "fieldType": "ACTION_NAME",
      "position": 5,
      "fieldComponents": []
    },
    {
      "id": "8",
      "name": {
        "en-GB": "Comment",
        "no-NB": "comment"
      },
      "active": true,
      "fieldType": "COMMENT_NOTIFICATION",
      "position": 6,
      "fieldComponents": []
    },
    {
      "id": "9",
      "name": {
        "en-GB": "Acknowledgement",
        "no-NB": "acknowledged"
      },
      "active": true,
      "fieldType": "ACKNOWLEDGEMENT",
      "position": 7,
      "fieldComponents": []
    },
    {
      "id": "11",
      "name": {
        "no-NB": "texteditor"
      },
      "active": true,
      "fieldType": "TEXTEDITOR",
      "position": 9,
      "fieldComponents": []
    },
    {
      "id": "14",
      "name": {
        "en-GB": "Task assignment"
      },
      "active": true,
      "fieldType": "TASK_ASSIGNMENT_SETUP",
      "required": true,
      "fieldComponents": [
        {
          "fieldComponentType": "PLANNED_HOURS",
          "enabled": true
        },
        {
          "fieldComponentType": "PLANNED_START_DATE",
          "enabled": true
        },
        {
          "fieldComponentType": "DUE_DATE",
          "enabled": true
        }
      ]
    }
  ]
}
```
 
From the dialog definition above we have the following field types. For each file type we will show the appropriate transition dialog field values you must pass.

### TEXTFIELD, TEXTAREA, TEXTEDITOR fields

The fields for the `TEXTFIELD`, `TEXTAREA` and `TEXTEDITOR` components are pretty straightforward to create an transition dialog entry. Given the `TEXTFIELD` dialog field definition below.

```json
{
  "id": "2",
  "name": {
    "no-NB": "textfield"
  },
  "active": true,
  "fieldType": "TEXTFIELD",
  "position": 0,
  "fieldComponents": []
}
```

Lets build the `transition` object to send to the API to transition between two states with a dialog containing this field.

```json
{
  "transitionId": "1",
  "dialog": {
    "dialogId": "1",
    "fields": [{
      "fileId": "2",
      "values": ["Text we are going to save"]
    }]
  }
}
```

This object will save the text entered for the field on the case. The same format for sending the value applies to `TEXTAREA` and `TEXTEDITOR`.

### NUMBER field

A `NUMBER` field is defined below.

```json
{
  "id": "4",
  "name": {
    "no-NB": "number"
  },
  "active": true,
  "fieldType": "NUMBER",
  "position": 2,
  "required": true,
  "fieldComponents": []
}
```

To set the value on the field for a `transition` create the following dialog object.

```json
{
  "transitionId": "1",
  "dialog": {
    "dialogId": "1",
    "fields": [{
      "fileId": "2",
      "values": ["10.0"]
    }]
  }
}
```

This will set field data to the string representation of the value 

### DATE field

A `DATE` field is defined below.

```json
{
  "id": "5",
  "name": {
    "no-NB": "date"
  },
  "active": true,
  "fieldType": "DATE",
  "position": 3,
  "fieldComponents": []
}
```

To set the value on the field for a `transition` create the following dialog object.

```json
{
  "transitionId": "1",
  "dialog": {
    "dialogId": "1",
    "fields": [{
      "fileId": "2",
      "values": ["2021-03-08T16:29:11.598Z"]
    }]
  }
}
```

Notice how the value is an ISO-8061 UTC formatted javascript date.

### PERFORM_TASK field

A `PERFORM_TASK` field is defined below.

```json
{
  "id": "6",
  "name": {
    "en-GB": "Perform Task",
    "no-NB": "perform_task"
  },
  "active": true,
  "fieldType": "PERFORM_TASK",
  "position": 4,
  "fieldComponents": []
}
```

To set the value on the field for a `transition` create the following dialog object.

```json
{
  "transitionId": "1",
  "dialog": {
    "dialogId": "1",
    "fields": [{
      "fileId": "2",
      "values": ["1", "2"]
    }]
  }
}
```

The values passed in the `values` field is the list of `userIds` that will perform the task. The server will validate that these users are valid users.

### ACTION_NAME field

A `ACTION_NAME` field is defined below.

```json
{
  "id": "7",
  "name": {
    "en-GB": "Action name",
    "no-NB": "action_name"
  },
  "active": true,
  "fieldType": "ACTION_NAME",
  "position": 5,
  "fieldComponents": []
}
```

To set the value on the field for a `transition` create the following dialog object.

```json
{
  "transitionId": "1",
  "dialog": {
    "dialogId": "1",
    "fields": [{
      "fileId": "2",
      "values": ["The action name"]
    }]
  }
}
```

The value passed in the `values` field is name of the `ACTION_ENTITY` that will be created when this dialog is triggered in a transition.

### COMMENT_NOTIFICATION field

A `COMMENT_NOTIFICATION` field is defined below. It allows us to send a comment as part of performing a transition betweeen two states.

```json
{
  "id": "8",
  "name": {
    "en-GB": "Comment",
    "no-NB": "comment"
  },
  "active": true,
  "fieldType": "COMMENT_NOTIFICATION",
  "position": 6,
  "fieldComponents": []
}
```

To set the value on the field for a `transition` create the following dialog object.

```json
{
  "transitionId": "1",
  "dialog": {
    "dialogId": "1",
    "fields": [{
      "fileId": "2",
      "values": ["The comment"]
    }],
    "users": ["1", "2", "3"]
  }
}
```

The value passed in the `values` field is comment text. We pass the list of `userIds` in the `users` field that will be notified about a new comment having been added.

### ACKNOWLEDGEMENT field

A `ACKNOWLEDGEMENT` field is defined below. It allows us to send a comment as part of performing a transition betweeen two states.

```json
{
  "id": "9",
  "name": {
    "en-GB": "Acknowledgement",
    "no-NB": "acknowledged"
  },
  "active": true,
  "fieldType": "ACKNOWLEDGEMENT",
  "position": 7,
  "fieldComponents": []
}
```

To set the value on the field for a `transition` create the following dialog object.

```json
{
  "transitionId": "1",
  "dialog": {
    "dialogId": "1",
    "fields": [{
      "fileId": "2",
      "values": ["1"]
    }]
  }
}
```

The value passed in the `values` field is the `userId` of the user who is approving the case. This applies primarely to cases that can be approved.

### TASK_ASSIGNMENT_SETUP field

A `TASK_ASSIGNMENT_SETUP` field is defined below. It allows us to assign a task to a set of users.

```json
{
  "id": "14",
  "name": {
    "en-GB": "Task assignment"
  },
  "active": true,
  "fieldType": "TASK_ASSIGNMENT_SETUP",
  "required": true,
  "fieldComponents": [
    {
      "fieldComponentType": "PLANNED_HOURS",
      "enabled": true
    },
    {
      "fieldComponentType": "PLANNED_START_DATE",
      "enabled": true
    },
    {
      "fieldComponentType": "DUE_DATE",
      "enabled": true
    }
  ]
}
```

To set the value on the field for a `transition` create the following dialog object.

```json
{
  "transitionId": "1",
  "dialog": {
    "dialogId": "1",
    "fields": [{
      "fileId": "2",
      "values": ["1", "2", "3"],
      "componentValues": [{
        "type": "PLANNED_START_DATE",
        "values": ["2021-03-08T16:29:11.598Z"]
      }, {
        "type": "DUE_DATE",
        "values": ["2021-03-08T16:29:11.598Z"]
      }, {
        "type": "PLANNED_HOURS",
        "values": ["10.0"]
      }]
    }]
  }
}
```

The values passed in the `values` field is the `userIds` of the users who will have a task assigned. The `componentValues` specifies values for the fields sub components. In this case we have three sub components `PLANNED_START_DATE`, `DUE_DATE` and `PLANNED_HOURS`.



