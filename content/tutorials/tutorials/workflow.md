---
title: "Creating a full workflow"
description: "In this tutorial we will create a full workflow and tie two together using the associated workflow support."
lead: In this tutorial we will create a full workflow and tie two together using the associated workflow support."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  tutorials:
    parent: "tutorials"
weight: 100
toc: true
---

## Creating an Action Workflow

We are going to create two workflows in this tutorial. The first one will be an action workflow that will handle actions that result from registered messages.

1. Lets start by clicking on the `Admin` menu on the left side. This will unfold the `Admin` menu.
2. Next click on the `Workflows` link to go to the overview of the workflows.
3. Next click the `New Workflow` button to initiate a new workflow creation.

{{< figure src="/images/workflow/workflow_1.png" caption="New workflow dialog" width="640">}}

Lets fill in the workflow title and entity type.

1. In the `Workflow title` enter `Action`
2. For the `Entity type` dropdown pick the `Action` entity type.

Next lets build the workflow itself. Click on the `Table` tab.

{{< figure src="/images/workflow/workflow_2.png" caption="New workflow table dialog" width="640">}}

There are three main sections when creating a new workflow. These are.

### Statuses

Statuses represent states in a process. An example of a state might be `New` for a new case and `Close for a closed state.

Click on the `Create status` button to open the `New status` dialog.

{{< figure src="/images/workflow/workflow_3.png" caption="New workflow status dialog" width="640">}}

We are going to create three new statuses for our `Action` workflow.

1. Write `Open` in the `Status name` field.
2. Next select the `Open` group.
3. Click on the `Save Changes` button to save the new status.

Next repeat it but this time.

1. Write `Being worked on` in the `Status name` field.
2. Next select the `In progress` group.
3. Click on the `Save Changes` button to save the new status.

Finally lets create the close status.

1. Write `Closed` in the `Status name` field.
2. Next select the `Closed` group.
3. Click on the `Save Changes` button to save the new status.

So what do the list of groups mean?

| Status Group | Description |
| --- | --- |
| `Open`<img width=200 height=1/> | A case is in a newly opened (first time it was opened state). This is basically used to signal a new case starting. |
| `Unprocessed` | A case has been created but not yet opened by any case handler. |
| `In progress` | A case is being worked on. |
| `In action process` | A case triggered an action process and is waiting for it to be resolved. |
| `Closed` | A case has been closed. |
| `Deleted` | A case has been deleted. |

You should now have a view that looks something like.

{{< figure src="/images/workflow/workflow_4.png" caption="Workflow table view 3 statuses" width="640">}}

### Transitions

### Dialogs

