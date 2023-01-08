---
title: "Creating a full workflow"
description: "In this tutorial we will create a full workflow and tie two together using the associated workflow support."
lead: "In this tutorial we will create a full workflow and tie two together using the associated workflow support."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 100
toc: true
---
## Action Workflow

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

Finally click the `Save` button in the top right corner to save the whole workflow.

### Dialogs

A dialog represents a set of fields configurable by the end user to collect information or trigger actions on a change of status for a case (a transition). Dialog are attached to transitions.

Lets create a dialog to allow us assign tasks and also comment on a case transition.

1. Click `Create Dialog` button to open the new dialog window.

{{< figure src="/images/workflow/workflow_5.png" caption="Workflow create new dialog" width="640">}}

2. Set the `Dialog name` to `Task assignment`.

Next lets look at what kind of fields we can add to the dialog and what they mean.

3. Click on the `Add field` button.

{{< figure src="/images/workflow/workflow_6.png" caption="Workflow add field to dialog" width="640">}}

As you can see there is a sizable selection of field types. Lets have a look at each and what they mean before constructing our custom dialog.

| Field Type | Triggers | Description |
| --- | --- | --- |
| `Textfield`<img width=200 height=1/> | No | A single row free text entry field. |
| `Textarea` | No | A text area with more columns for free text entry. |
| `Text Editor` | | A text area with basic formatting for free text entry. |
| `Number` | No | Entering any numeric value. |
| `Date` | No | Specifiying a date. |
| `Perform Task` | Yes | A field allowing you to specify who performed the task. |
| `Action Name` | Yes | The title field that will be used when creating a new `Action` entry for a transition going into an `In action process` group state |
| `Comment` | Yes | Allows the user to comment on the transition between states and set who is getting notified about the comment. |
| `Acknowledgement` | Yes | Lets the user acknowledge that specific users performed their tasks. |
| `Task Assignment Setup` | Yes | Allows the user to create tasks of a specific type when transitioning between statues. One can also control if one wants to collect a `Due date`, `Planned hours` and `Planned start date`. |

4. Add a field of type `Task Assignment` to the `Dialog`. `Due date`, `Planned start date` and `Planned hours`. Set the `Case participant type` dropdown to the value `Case Participator`. Leave the box `Required` unchecked.

5. Add a field of type `Comment` to the `Dialog`. Leave `Required` unchecked.

6. Click `Save Changes` to add the dialog to the workflow.

Next lets create an approval dialog.

1. Click `Create Dialog` button to open the new dialog window.
2. Set the `Dialog name` to `Approval`.
3. Add a field of type `Acknowledgement` to the `Dialog`. Leave the box `Required` unchecked.
4. Add a field of type `Comment` to the `Dialog`. Leave `Required` unchecked.
5. Click `Save Changes` to add the dialog to the workflow.

Your workflow screen should look something like this now.

{{< figure src="/images/workflow/workflow_7.png" caption="Workflow create new dialog" width="640">}}

Finally click the `Save` button in the top right corner to save the whole workflow.

### Transitions

A transition represents a change between two statuses (As an example you might move a case from `Open` status to `Being worked on` status).

A transition can have an optional dialog attached to it to collect information as part of the transition.

When we talk about transitions we will use `source` as the start status of the transition and `target` as the end status.

The `target` status has a `Status group` that will trigger actions during the transition.

| Status Group | Actions |
| --- | --- |
| `Open`<img width=200 height=1/> | When a case is transitioned into the Open group it will possibly trigger notifications to the picked case handler for the case. |
| `Unprocessed` | Might trigger notifications to the target case handler. |
| `In progress` | Usually does not trigger actions. |
| `In action process` | Will trigger the creation of an `Action entry` with its new workflow and potentially notifications. |
| `Closed` | Might trigger notifications to the target case handler. |
| `Deleted` | Might trigger notifications to the target case handler. |

Lets create a table that shows the transitions we will build.

| From status | To status | Dialog | Description |
| --- | --- | ---- | ---- |
| `Open` | `Being worked on` | `Task assignment` | Lets us move a case into the in progress group state. |
| `Being worked on` | `Being worked on` | `Task assignment` | Lets us move a case into the in progress group state. |
| `Being worked on` | `Closed` | `Approval` | Lets us move a case into the closed status. |

Lets click on the `Create Transition` button to bring up create transition dialog.

{{< figure src="/images/workflow/workflow_8.png" caption="Workflow create new transition" width="640">}}

#### Build Open to Being worked on
1. Fill in the `Transition name` field with `Start work`.
2. Select the `Open` status as the `From status` and `Being worked on` as the `To status`.
3. Select the `Task assignment` dialog.
4. Click the `Save changes` button.

#### Being worked on to Being worked on
1. Fill in the `Transition name` field with `Being worked on`.
2. Select the `Being worked on` status as the `From status` and `Being worked on` as the `To status`.
3. Select the `Task assignment` dialog.
4. Click the `Save changes` button.

#### Being worked on to Closed
1. Fill in the `Transition name` field with `Close`.
2. Select the `Being worked on` status as the `From status` and `Close` as the `To status`.
3. Select the `Approval` dialog.
4. Click the `Save changes` button.

Finally click the `Save` button in the top right corner to save the whole workflow.

You should now have a workflow that looks like the following.

{{< figure src="/images/workflow/workflow_9.png" caption="Complete workflow table" width="640">}}

### Finish Action workflow

Finally click on the `General` tab and set the `Start case status` pulldown to `Open` and `Close case status` to `Close`. These options signal the start and end points of the workflow.

{{< figure src="/images/workflow/workflow_11.png" caption="Complete workflow" width="640">}}

Finally click the `Save` button to save the whole workflow.

### Graph

Finally we can see a graphical representation of the workflow by clickin on the `Graph` tab. Clicking on the tab will show you someting looking like.

{{< figure src="/images/workflow/workflow_10.png" caption="Workflow graph representation" width="640">}}

## Message Workflow

Next we are going to build a message workflow. Lets outline what we plan to build and follow the steps mentioned above to build the actual statuses, dialogs and transitions.

1. Click `New workflow`.
2. In the `Workflow title` enter `Message`
3. For the `Entity type` dropdown pick the `Message` entity type.

### Statuses

We are going to create the following statuses.

| Name | Group type | Description |
| --- | --- | --- |
| `Open` | `Open` | The initial state for a new case. |
| `Being worked on` | `In progress` | The case is being worked on. |
| `To action` | `In action process` | The action resulting from the message is being worked on. |
| `Closed` | `Closed` | We finished working on the message. |

### Dialogs

We are going to build the following dialogs.

#### Assign case

Next lets create an approval dialog.

1. Click `Create Dialog` button to open the new dialog window.
2. Set the `Dialog name` to `Assign case`.
3. Add a field of type `Task Assignment` to the `Dialog`. Leave the box `Required` unchecked.
4. Add a field of type `Comment` to the `Dialog`. Leave `Required` unchecked.
5. Click `Save Changes` to add the dialog to the workflow.

#### Create action

Next lets create an create action dialog.

1. Click `Create Dialog` button to open the new dialog window.
2. Set the `Dialog name` to `Create action`.
3. Add a field of type `Action Name` to the `Dialog`. Leave the box `Required` checked.
4. Add a field of type `Task assignment` to the `Dialog`. Leave `Required` unchecked.
5. Add a field of type `Comment` to the `Dialog`. Leave `Required` unchecked.
6. Click `Save Changes` to add the dialog to the workflow.

#### Close

Next lets create an create action dialog.

1. Click `Create Dialog` button to open the new dialog window.
2. Set the `Dialog name` to `Close`.
3. Add a field of type `Acknowlegement` to the `Dialog`. Leave `Required` checked.
4. Add a field of type `Comment` to the `Dialog`. Leave `Required` unchecked.
5. Click `Save Changes` to add the dialog to the workflow.

At the end your workflow should looking something like.

{{< figure src="/images/workflow/workflow_12.png" caption="Workflow dialogs overview" width="640">}}

### Transitions

We will add the following transitions to our workflow.

| Name | From status | To status | Dialog | Description |
| --- |--- | --- | ---- | ---- |
| **Open** | `Open` | `Being worked on` | `Assign case` | Lets us move a case into the in progress group state. |
| **Being worked on** | `Being worked on` | `Being worked on` | `Assign case` | Lets us move a case into the in progress group state. |
| **To action** | `Being worked on` | `To action` | `Create action` | Lets us move a case into the closed status. |
| **To action** | `To action` | `To action` | `Create action` | Lets us create more actions from a given message. |
| **Being worked on** | `To action` | `Being worked on` | `Assign case` | Move the message back into Being worked on. |
| **Close** | `Being worked on` | `Closed` | `Close` | Close the message case. |
| **Close** | `To action` | `Closed` | `Close` | Close the message case. |

{{< figure src="/images/workflow/workflow_13.png" caption="Workflow dialogs overview" width="640">}}


