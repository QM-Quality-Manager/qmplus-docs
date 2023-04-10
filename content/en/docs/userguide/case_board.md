---
title: "Cases board"
description: "A user guide for working with the Cases boards"
lead: "A user guide for working with the Cases boards. We cover how to create, update and manage Cases boards."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 2
toc: true
---
This section deals with using the Cases board.

Clicking on the `Cases board` gives access to Cases board.

## Handling the Case board

{{< figure src="/images/case_board/case_board_1.png" caption="case_board_1.png" width="1024">}}

The case board is the easiest and powerful way of managing cases for workflows. It lets you move cases between states easily, filter the board by different criteria and access the case information.

| Option | Description |
| --- | --- |
| `Select the workflow` | Select between the workflows you have access to, allowing you to switch between case boards. |
| `Case status` | The workflow case statuses, are laid out as columns where cases in that status group is laid out. The exception is the `Close` case status columns where they are grouped by week to avoid information overload. |
| `Collapse/Expand the column` | User can collapse/expand the columns to lessen the information density of the screen. |
| `Case` | Each box represents a current case in the system. The user can click on the case to bring up the quick view of the case details. The ... menu on the case box allows access to a menu over statuses the case is allowed to move to. |
| `Search` | The top right search box lets you filter the cases visible on the board by searching the title and description of the cases avaialble.|

### Case Status Transition

{{< figure src="/images/case_board/case_board_6.png" caption="case_board_6.png" width="1024">}}

To move cases you can grab a case and drag it to a new status. 

{{< figure src="/images/case_board/case_board_3.png" caption="case_board_3.png" width="1024">}}

If the transition from the existing case status to the new case status requires filling in a dialog it will pop up and has to be completed before the case is moved to the new state.

{{< figure src="/images/case_board/case_board_5.png" caption="case_board_5.png" width="1024">}}

You can also move a case by clicking the hamburger menu on the top right corner of each case and then selecting one of the allowed state transitions.

### View Case Information

{{< figure src="/images/case_board/case_board_4.png" caption="case_board_4.png" width="1024">}}

When clicking on a case in the case board we get the `compact case view`. You can click on the arrow icon in the top right corner of the `compact case view` to open the full case view. There are a fair bit of options in the `compact case view`.

| Option | Description |
| --- | --- |
| `Title` | Clicking directly on the title will let the user edit the title for the case. |
| `Description` | The user can edit the description of the case and click the `Save` button to save the changes. |
| `Comment` | The comment section let the user add a quick comment to the case, use the `Notify` button to select users to notify about the new comment and then click `Comment` to save the comment to the case and send a notification to all the users selected. |
| `Case handler` | Change or set the current case handler. |
| `Case approver` | Change or set the current case approver. |
| `Case status` | Change the case status of the case. |
| `Department` | Change the current department of the case. |
| `Priority` | Change the current priority of the case. |
| `Tasks` | See all pending tasks on the case and allow the user to change the state of each task. |

## Caseboard filters

{{< figure src="/images/case_board/case_board_2.png" caption="case_board_2.png" width="1024">}}

The slideout options menu on the left lets us filter the board down depending on our needs. It contains multiple pre-defined filters.

| Pre-defined filter | Description |
| --- | --- |
| `Handled by me` | All cases where the current logged in user is the case handler. |
| `Approved by me` | All cases where the current logged in user is the approver. |
| `Participated in by me` | All cases where the current logged in user is a case participant. |
| `No case handler` | All cases that have no current case handler. |
| `No case approvers` | All cases that have no current case approver. |
| `No tasks` | All cases that have no associated tasks with them. |
| `Overdue` | All overdue cases. |
| `Updated today` | All cases updated today. |
| `Updated in last week` | All cases updated during the last week. |
| `Created today` | All cases created today. |
| `Created in last week` | All cases created during the last week. |

There are several additional filters that can be used that vary depending on the type of workflow (if it's a message, action, document, hearing or audit workflow).

| Filter | Entity Types | Description |
| --- | --- | --- |
| `Case approvers` | `All` | Add case approver users to filter by. Will show cases that have at least one of the users added as an approver. |
| `Case handler` | `All` | Add case chandler users to filter by. Will show cases that have at least one of the users added as a case handler. |
| `Case category` | `Message` | Locate cases that contain one or more of the categories selected, can be used to filter cases looking for specific message cases for a given category. |
