---
title: "Administrator/Forms"
description: "A user guide for working with forms"
lead: "A user guide for working with forms. We cover how to create and modify forms."
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
This section deals with managing forms in the system.

Clicking on the `Administrator/Forms` gives access to the list of forms.

## Forms Listing

{{< figure src="/images/forms/forms_1.png" caption="List of all current forms" width="1024">}}

Shows the list of forms registered in the system. You can filter by `Active`, `Inactive` and `All` forms as well as search by text. For more filtering options. you can click the apply filter button to bring up the sidebar.

{{< figure src="/images/forms/forms_9.png" caption="Filter form list" width="1024">}}

We have the following filters available for the forms listing.

| Filter | Description |
| --- | --- |
| `Visibility` | Filter by the forms visibility type (`Department`, `Department and children` etc.) |
| `Form type` | Filter the forms by the form type. |

## Create a new Form

{{< figure src="/images/forms/forms_2.png" caption="" width="1024">}}

To create a new form we need to specify the following fields.

| Field | Required | Description |
| --- | --- | --- |
| `Form title` | **X** | The title of the form, supports multiple languages. |
| `Form type` | **X** | Select one of the `Form Types` from our system. |
| `Anonymity` | **X** | Select if the form support anonymous entry of data. |
| `Visibility` | **X** | Set the visibility for the form. |
| `Department` | **X** | Set the department where the form is visible from. |
| `Device platform visibility` | |  Allow selecting the platforms the form is available on (Web, Mobile, All), No selection means All and is the default. |
| `Tasks Templates` | | Select an optional `Tasks Template` that will create a set of tasks on a case when a new form registration happens. |
| `Description` | | A long text description for the form, support multiple languages. |
| `Button text` | | The text shown in the register form menu, support multiple languages. |
| `References` | | Add document references to the form from your document library. |
| `Permissions` | | Lock down the form based on system or custom permissions. |

## Build Form

{{< figure src="/images/forms/forms_4.png" caption="" width="1024">}}

The `Layout Tab` lets start building the `Form` using components.

When clicking `Create New Item` we get a pop up menu that outlines the available components.

{{< figure src="/images/forms/forms_7.png" caption="" width="1024">}}

The available components you can add are.

| Component | Description |
| --- | --- |
| `Registered by` | Shows the person who registered the form entry. |
| `Date/Time` | Add a field to record a date and time combination. |
| `Registered on behalf of` | Allows the person entering the form to specify who they are entering the registration on behalf of. |
| `Registered on department` | On what department should the form entry be registered. |
| `Choose case handler` | Lets the person entering the form choose a case handler directly routing it to a person to work on. |
| `Describe the circumstances/deviation here` | Text description for used to describe the circumstances/deviation. |
| `Cost of fault until now` | The estimated cost in monetary value until now. | 
| `Priority` | Allows the user to specify a priority for the form entry. | 
|||
| `Defining category group` | Adds a defining category group to the form. |
| `Category group` | Adds a normal category group to the form. |
| `Label` | A text label to add structure to the form. |
|||
| `File` | A file upload component, allowing the end user to upload a file. |
| `Image` | Add an image to the form. For example a diagram of instructions. |
| `Manual Signature` | A field that accepts manual signatures. |
|||
| `Text field` | A oneline text field. |
| `Rich text editor field` | A rich text editor field. |

A form can have a single, double or triple colum layout.

> For mobile only forms we recommend a single colum but mobile client also support changing columns.

### Configuring a Category Component

{{< figure src="/images/forms/forms_8.png" caption="" width="1024">}}

A category group has several configuration options.

| Options | Description |
| --- | --- |
| `Render type` | How to render the category group. |
| `Mandatory` | Is the category group mandatory. |
| `Only visible in case overflow` | Only visible for case handlers. Not visible for person entering a form. |
| `Visible on mobile` | Is visible on mobile. |
|||
| `Override visiblity` | Override the forms visiblity for this category group only. Say you want to show a category group only for a sub department. |
| `Visibility` | Set the override visibility. |
| `Department` | Set the override department. |
|||
| `Category group` | The category group allows the designer to select a subset of categories to show in the form. |

The available render types are.

| Options | Description |
| --- | --- |
| `Auto` | Selected the component most appropriate depending on the number of categories. If there are a lot of categories it will switch to dropdown automatically. |
| `Dropdown` | Dropdown menu of categories. |
| `Radio buttons` | Radio buttons for `single-select` categories. |
| `Check boxes` | Check boxes for `multi-select` category groups. |

### Configuring a Text Element

{{< figure src="/images/forms/forms_12.png" caption="" width="1024">}}

A text element has several configuration options.

| Options | Description |
| --- | --- |
| `Mandatory` | Is the category group mandatory. |
| `Only visible in case overflow` | Only visible for case handlers. Not visible for person entering a form. |
| `Visible on mobile` | Is visible on mobile. |
| `Barcode read support` | Enables barcode scanning support for the field. |
| `Max length` | Maximum length of the text field. |
|||
| `Override visiblity` | Override the forms visiblity for this category group only. Say you want to show a category group only for a sub department. |
| `Visibility` | Set the override visibility. |
| `Department` | Set the override department. |

## Form Preview

{{< figure src="/images/forms/forms_5.png" caption="" width="1024">}}

Form preview lets you test how the form behaves.

| Mode | Description |
| --- | --- |
| `During registration` | This is how the form is seen by the user entering a form. |
| `During case handling` | This is how the form is seen by a case handler after opening the registered form entry. |

> You can change the department by clicking on the department at the top right corner. This lets you see how the form will render on different departments.

{{< figure src="/images/forms/forms_6.png" caption="" width="1024">}}

## Processing Settings

The processing tab contains setting to set defaults for case deadlines and escalations for this particular form. This overrrides any settings specified at the workflow level if set.

{{< figure src="/images/forms/forms_3.png" caption="" width="1024">}}

### Due dates

Allows the control of how due date notifications are handled. This allows one to set general due date handling settings for this workflow and thus `forms` using this workflow.

> `Forms` let you override these so you can for example have a form `Accident` that have much shorter automatic due dates compared to the general workflow. `Form` settings will override the workflow.

The available fields.

| Field | Description |
| --- | --- |
| `Number of days before overdue` | The number of days since the last update happened to a case before it's considered overdue. |
| `Reminder email frequencey` | The frequence of sending overdue email notifications. These are options like `Off`, `Every day`, `Everyone Monday` etc. |
| `Time of day to send overdue emails` | Specify the time of day to send the email. For example you might overdue notices to be delivered after 9 in the morning. This is not an exact time. The email some time after the specified time depending on your email system and sending time. |

### Escalation

Allows the control of how escalations are handled. This allows one to set general escalation handling settings for this workflow and thus `forms` using this workflow.

> `Forms` let you override these so you can for example have a form `Accident` that have much shorter automatic escalation date compared to the general workflow. `Form` settings will override the workflow.

The available fields.

| Field | Description |
| --- | --- |
| `Escalation of overdue cases enabled` | Enable or disable the escalation. |
| `Escalate after N hours overdue` | The number of hours since the last case update happened before it's considered for escalation. |
| `Escalation strategy` | The strategy to pick to whom to escalate the case. See available strategies below. |
| `Time of day to escalate mesages` | What time of the day to escalate messages. |
| `Number of hours for next due date after escalation` | The next due date after escalating the case to a new case handler. |

The available strategies.

| `Direct supervisor` | The case will be sent to the persons closest direct supervisor with permission to process cases. If there are more than one potential supervisor it will pick on of them on random. |


