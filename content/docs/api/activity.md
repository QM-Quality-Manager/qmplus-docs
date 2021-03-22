---
title: "Activity"
description: "Covering the Activity API."
lead: "Covers use of the Activity API."
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

This section covers operating on `Activities` in qmplus.

The relevant swagger information is located at.

[Swagger Calendar API](https://app.qmplus.com/swagger-ui/index.html?contextPath=&requestServerName=app.qmplus.com#/activities)

## Creating Basic Activities

The activity operation are more complex than the `Calendar` operation as there are a lot of options. In this section we will outline the options and show how you can create a couple of different activies as well as explain an activity tree structure.

### Single Activity

Lets look at how we can create a basic activity with a single date entry.

```json
{
  "visibility": "DEPARTMENT",
  "departmentId": "1",
  "name": {
        "en_US": "Remember to fill in form A"
  },
  "belongsTo": "CALENDAR",
  "belongsToId": "1",
  "periodicity": {
    "type": "SINGLE",
    "start": "2021-03-01T14:40:00.838Z",
    "end": "2021-03-01T16:40:00.838Z"
  }
}
```

This will create a single activity on the `Calendar` with `calendarId` equal to `1`. Below is an example curl for creating an activity with the data above.

```bash
curl -X POST "https://app.qmplus.com/api/activity" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 10000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"visibility\": \"DEPARTMENT\", \"departmentId\": \"1\", \"name\": { \"en_US\": \"Remember to fill in form A\" }, \"belongsTo\": \"CALENDAR\", \"belongsToId\": \"1\", \"periodicity\": { \"type\": \"SINGLE\", \"start\": \"2021-03-01T14:40:00.838Z\", \"end\": \"2021-03-01T16:40:00.838Z\" }}"
```

> Creating an activity will add it to the existing calendar object. If you fetch the `Calendar` object with `id = 1` it will include the new activity id in it's list of activities.

### Multiple Activities

In this example we will create multiple activity entries for a given activity. Lets say you have an activity called `Evaluate Engine`, you might need to two meetings on specific dates. This form of Activity lets you create multiple entries.

```json
{
  "visibility": "DEPARTMENT",
  "departmentId": "1",
  "name": {
        "en_US": "Evaluate Engine"
  },
  "belongsTo": "CALENDAR",
  "belongsToId": "1",
  "periodicity": {
    "type": "MULTIPLE",
    "dates": [{
      "start": "2021-03-01T14:40:00.838Z",
      "end": "2021-03-01T16:40:00.838Z"
    }, {
      "start": "2021-04-01T14:40:00.838Z",
      "end": "2021-04-01T16:40:00.838Z"
    }]
  }
}
```

The equivalent curl operation.

```bash
curl -X POST "https://app.qmplus.com/api/activity" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 10000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"visibility\": \"DEPARTMENT\", \"departmentId\": \"1\", \"name\": { \"en_US\": \"Evaluate Engine\" }, \"belongsTo\": \"CALENDAR\", \"belongsToId\": \"1\", \"periodicity\": { \"type\": \"MULTIPLE\", \"dates\": [{ \"start\": \"2021-03-01T14:40:00.838Z\", \"end\": \"2021-03-01T16:40:00.838Z\" }, { \"start\": \"2021-04-01T14:40:00.838Z\", \"end\": \"2021-04-01T16:40:00.838Z\" }] }}"
```

## Creating Periodic Activities

There are several types of Periodic activites that be created. Below we show some examples of how to create periodic activities.

### Periodic Activity on Mondays

In this example we are going to create an activity that happens once a week for the next 5 weeks.

```json
{
  "visibility": "DEPARTMENT",
  "departmentId": "1",
  "name": {
        "en_US": "Evaluate Engine"
  },
  "belongsTo": "CALENDAR",
  "belongsToId": "1",
  "periodicity": {
    "type": "PERIOD",
    "periodType": "WEEKLY",
    "start": "2021-03-01T14:40:00.838Z",
    "end": "2021-03-01T16:40:00.838Z",
    "endAtDate": "2021-04-06T16:40:00.838Z"
  }
}
```

The equivalent curl operation.

```bash
curl -X POST "https://app.qmplus.com/api/activity" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 10000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"visibility\": \"DEPARTMENT\", \"departmentId\": \"1\", \"name\": { \"en_US\": \"Evaluate Engine\" }, \"belongsTo\": \"CALENDAR\", \"belongsToId\": \"1\", \"periodicity\": { \"type\": \"PERIOD\", \"periodType\": \"WEEKLY\", \"start\": \"2021-03-01T14:40:00.838Z\", \"end\": \"2021-03-01T16:40:00.838Z\", \"endAtDate\": \"2021-04-06T16:40:00.838Z\" }}"
```

This will create entiries until it reaches the `endAtDate` specified.

> You can alternatively use `endAfterTimes` to specify how many instances you want to create instead of using an end date.

### Periodic Yearly Activity

In this example we are going to create an activity that happens once a year but will place as close as it can to a full year but keeping the original day of the week.

```json
{
  "visibility": "DEPARTMENT",
  "departmentId": "1",
  "name": {
        "en_US": "Evaluate Engine"
  },
  "belongsTo": "CALENDAR",
  "belongsToId": "1",
  "useSameDayOfWeekAsStartDate": true,
  "periodicity": {
    "type": "PERIOD",
    "periodType": "YEARLY",
    "start": "2021-03-01T14:40:00.838Z",
    "end": "2021-03-01T16:40:00.838Z",
    "endAfterTimes": 3
  }
}
```

The equivalent curl operation.

```bash
curl -X POST "https://app.qmplus.com/api/activity" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 10000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"visibility\": \"DEPARTMENT\", \"departmentId\": \"1\", \"name\": { \"en_US\": \"Evaluate Engine\" }, \"belongsTo\": \"CALENDAR\", \"belongsToId\": \"1\", \"useSameDayOfWeekAsStartDate\": true, \"periodicity\": { \"type\": \"PERIOD\", \"periodType\": \"YEARLY\", \"start\": \"2021-03-01T14:40:00.838Z\", \"end\": \"2021-03-01T16:40:00.838Z\", \"endAfterTimes\": 3 }}"
```

This will create entiries until it reaches the `endAfterTimes` specified.

### Periodic Activity on Specific Weekdays

In this example we going to create an activity that will only happen on Monday, Wednesday and Friday and only for 5 weeks.

```json
{
  "visibility": "DEPARTMENT",
  "departmentId": "1",
  "name": {
        "en_US": "Evaluate Engine"
  },
  "belongsTo": "CALENDAR",
  "belongsToId": "1",
  "periodicity": {
    "type": "PERIOD",
    "days": ["MONDAY", "WEDNESDAY", "FRIDAY"],
    "start": "2021-03-01T14:40:00.838Z",
    "end": "2021-03-01T16:40:00.838Z",
    "endAfterTimes": 5
  }
}
```

The equivalent curl operation.

```bash
curl -X POST "https://app.qmplus.com/api/activity" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 10000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"visibility\": \"DEPARTMENT\", \"departmentId\": \"1\", \"name\": { \"en_US\": \"Evaluate Engine\" }, \"belongsTo\": \"CALENDAR\", \"belongsToId\": \"1\", \"periodicity\": { \"type\": \"PERIOD\", \"days\": [\"MONDAY\", \"WEDNESDAY\", \"FRIDAY\"], \"start\": \"2021-03-01T14:40:00.838Z\", \"end\": \"2021-03-01T16:40:00.838Z\", \"endAfterTimes\": 5 }}"
```

## Attaching Artefacts

An activity is great by itself but not particularily useful without related attachments. In this example we are going to create an Activity that contains a set of associated artefacts. We will attach a questionnaire, form and a document.

### Basic Artefacts

Adding an activity with basic artefacts. The types available are.

| Name | Description |
| --- | --- |
| `FORM` | Attach a form with specific version |
| `QUESTIONNAIRE` | Attach a questionnaire that must be peformed with this activity |
| `DOCUMENT` | Attach a doument that is related to this activity |

```json
{
  "visibility": "DEPARTMENT",
  "departmentId": "1",
  "name": {
        "en_US": "Do some work"
  },
  "belongsTo": "CALENDAR",
  "belongsToId": "1",
  "periodicity": {
    "type": "SINGLE",
    "start": "2021-03-01T14:40:00.838Z",
    "end": "2021-03-01T16:40:00.838Z"
  },
  "artifacts": [{
    "type": "FORM", "id": "1", "version": 1, "description": { "en_US": "Artefact 1" }
  }, {
    "type": "QUESTIONNAIRE", "id": "1", "version": 1, "description": { "en_US": "Artefact 2" }
  }, {
    "type": "DOCUMENT", "id": "1", "version": 1, "description": { "en_US": "Artefact 3" }
  }]
}
```

The equivalent curl operation.

```bash
curl -X POST "https://app.qmplus.com/api/activity" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 10000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"visibility\": \"DEPARTMENT\", \"departmentId\": \"1\", \"name\": { \"en_US\": \"Do some work\" }, \"belongsTo\": \"CALENDAR\", \"belongsToId\": \"1\", \"periodicity\": { \"type\": \"SINGLE\", \"start\": \"2021-03-01T14:40:00.838Z\", \"end\": \"2021-03-01T16:40:00.838Z\" }, \"artifacts\": [{ \"type\": \"FORM\", \"id\": \"1\", \"version\": 1, \"description\": {} }, { \"type\": \"QUESTIONNAIRE\", \"id\": \"1\", \"version\": 1, \"description\": {} }, { \"type\": \"DOCUMENT\", \"id\": \"1\", \"version\": 1, \"description\": {} }]}"
```

This will create an `Activity` that contains three artefacts. Next lets create an Activity that is only visible to specific people using the `CreateContext` to limit the distribution of the activity.

### Restrict Activity

We can control who has access to the activity by using the `CreateContext` to specify the following lists of values.

| Name | Description |
| --- | --- |
| `userIds` | A list of userIds that will get the activity |
| `roleGroupIds` | A list of role groups that will be used to determine the users that have access to the activity |
| `roleIds` | A list of roles that will be used to determine the users that have access to the activity |
| `departmentIds` | A list of departmentId's that will be used to fetch users |

```json
{
  "visibility": "DEPARTMENT",
  "departmentId": "1",
  "name": {
        "en_US": "Do some work"
  },
  "belongsTo": "CALENDAR",
  "belongsToId": "1",
  "periodicity": {
    "type": "SINGLE",
    "start": "2021-03-01T14:40:00.838Z",
    "end": "2021-03-01T16:40:00.838Z"
  },
  "context": {
    "userIds": ["1", "2", "3"]
  },
  "artifacts": [{
    "type": "FORM", "id": "1", "version": 1
  }, {
    "type": "QUESTIONNAIRE", "id": "1", "version": 1
  }, {
    "type": "DOCUMENT", "id": "1", "version": 1
  }]
}
```

The equivalent curl operation.

```bash
curl -X POST "https://app.qmplus.com/api/activity" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 10000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"visibility\": \"DEPARTMENT\", \"departmentId\": \"1\", \"name\": { \"en_US\": \"Do some work\" }, \"belongsTo\": \"CALENDAR\", \"belongsToId\": \"1\", \"periodicity\": { \"type\": \"SINGLE\", \"start\": \"2021-03-01T14:40:00.838Z\", \"end\": \"2021-03-01T16:40:00.838Z\" }, \"context\": { \"userIds\": [\"1\", \"2\", \"3\"] }, \"artifacts\": [{ \"type\": \"FORM\", \"id\": \"1\", \"version\": 1 }, { \"type\": \"QUESTIONNAIRE\", \"id\": \"1\", \"version\": 1 }, { \"type\": \"DOCUMENT\", \"id\": \"1\", \"version\": 1 }]}"
```

### Set Notficiation Settings

Lets take the activity from above and add some notification information notifying us 2 days before the activity at 13:00.

```json
{
  "visibility": "DEPARTMENT",
  "departmentId": "1",
  "name": {
        "en_US": "Do some work"
  },
  "belongsTo": "CALENDAR",
  "belongsToId": "1",
  "periodicity": {
    "type": "SINGLE",
    "start": "2021-03-01T14:40:00.838Z",
    "end": "2021-03-01T16:40:00.838Z"
  },
  "context": {
    "userIds": ["1", "2", "3"]
  },
  "notifications": {
    "periodType": "DAILY",
    "types": ["EMAI"],
    "unitsBefore": 7,
    "time": "2021-03-01T13:00:00.838Z"
  },
  "artifacts": [{
    "type": "FORM", "id": "1", "version": 1
  }, {
    "type": "QUESTIONNAIRE", "id": "1", "version": 1
  }, {
    "type": "DOCUMENT", "id": "1", "version": 1
  }]
}
```

The equivalent curl operation.

```bash
curl -X POST "https://app.qmplus.com/api/activity" -H "accept: application/json" -H "auth-impersonate-tenant-id: 104" -H "auth-impersonate-user-id: 10000001" -H "auth-tenant-id: 0" -H "auth-token: TOKEN" -H "Content-Type: application/json" -d "{ \"visibility\": \"DEPARTMENT\", \"departmentId\": \"1\", \"name\": { \"en_US\": \"Do some work\" }, \"belongsTo\": \"CALENDAR\", \"belongsToId\": \"1\", \"periodicity\": { \"type\": \"SINGLE\", \"start\": \"2021-03-01T14:40:00.838Z\", \"end\": \"2021-03-01T16:40:00.838Z\" }, \"context\": { \"userIds\": [\"1\", \"2\", \"3\"] }, \"notifications\": { \"periodType\": \"DAILY\", \"types\": [\"EMAI\"], \"unitsBefore\": 7, \"time\": \"2021-03-01T13:00:00.838Z\" }, \"artifacts\": [{ \"type\": \"FORM\", \"id\": \"1\", \"version\": 1 }, { \"type\": \"QUESTIONNAIRE\", \"id\": \"1\", \"version\": 1 }, { \"type\": \"DOCUMENT\", \"id\": \"1\", \"version\": 1 }]}"
```

