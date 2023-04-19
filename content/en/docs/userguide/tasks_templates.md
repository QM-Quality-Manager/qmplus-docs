---
title: "Administrator/Task Templates"
description: "A user guide for working with Task Templates"
lead: "A user guide for working with Task Templates. We cover how to create and modify Task Templates."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 15
toc: true
---
This section deals with managing Task Templates in the system.

Clicking on the `Administrator/Task Templates` gives access to the list of Task Templates.

`Tasks Templates` lets you create list of tasks that will be added to new `Case` when a `Message` is registered. For example you might make a list of tasks that must be performed each time an accident message is logged in the system.

You can also add additional tasks only if certain categories are selected by the user when filling in the form. This lets you create dynamic tasks templates that can add additional tasks depending on the form entry itself.

> Tasks Templates is a very powerful way of ensuring tasks checklists are standardized across the organization for given `Form` entries.

## Tasks Templates Listing

{{< figure src="/images/tasks_templates/tasks_templates_2.png" caption="" width="1024">}}

The `Tasks Templates` listing shows you all the current `Tasks Templates` you can view.

> The listing will change as you change department in the organization as `Tasks Templates` can be registered on a specific department and given a organizational visibility type (visible on department, visible on department and child departments, etc.)

## Create a new Task Template

{{< figure src="/images/tasks_templates/tasks_templates_3.png" caption="" width="1024">}}

When creating a new Tasks Template we have the following options.

| Option | Description |
| --- | --- |
| `Tasks Template name` | Set the name to identify the `Tasks` template, support multiple languages. |
| `Description` | Set the description for the `Tasks` template. |
| `Visibility` | Set the organizational visibility (department, department and child departments). |
| `Department` | The department the `Tasks` template is registered on. |
| `Add Task` | Add a `Template` task to the `Tasks` template. |

Click the `Save` button to save the current state of the `Tasks Template`.

### Adding a new Task

{{< figure src="/images/tasks_templates/tasks_templates_4.png" caption="" width="1024">}}

Clicking the `Add Task` brings up the sidebar with the options for a new Task. The following options are available.

| Option | Description |
| --- | --- |
| `Name` | Name of the task to be added to the `Tasks` templates. |
| `Categories` | List of categories that will trigger the addition of this particular case to a new `Case` when a form message is registered. |

Click the `Configure` button to retrieve the list of available categories. Finally click the `Save Changes` button to save the `Task` to the `Tasks Template`.

### Select Categories

{{< figure src="/images/tasks_templates/tasks_templates_5.png" caption="" width="1024">}}

After clicking the `Configure` button you can search and select the categories that will trigger the addition of the `Task` being created.

## Editing a Tasks Template

{{< figure src="/images/tasks_templates/tasks_templates_6.png" caption="" width="1024">}}

When editing a `Tasks Template` you can drag the individual tasks up and down to re-order the tasks in whatever order you want them to be when added to a `Case`.

> We recommend not starting names with a number if one uses the `categories` filter as it might make for lists that can be missing continuity. Say you add task 1. A, 2. B, 3. C and task 2 is dependent on a category you might end up with a `Case` task list that only contains 1. A and 3. C confusing users.

You can also `Edit`, `View` and `Delete` individual task in the `Tasks Template`.

## Mapping Tasks Template to Form

{{< figure src="/images/tasks_templates/tasks_templates_8.png" caption="" width="1024">}}

When creating or editing a `Form` you can choose an optional associated `Tasks Template` from the list of templates visible for the current users department.

{{< figure src="/images/tasks_templates/tasks_templates_9.png" caption="" width="1024">}}

When a user registeres a new message of this form the `Case` will contain a list of `Tasks` based on the associated `Tasks Template`.
