---
title: "Administrator/Form Types"
description: "A user guide for working with form types"
lead: "A user guide for working with form types. We cover how to create and modify form types."
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
This section deals with managing form types in the system.

Clicking on the `Administrator/Form Types` gives access to the list of form types.

`Form Types` serve as a grouping of `forms` allowing us to set some settings that will be shared by all the forms based on a specific form type.

## Risk models List

{{< figure src="/images/form_types/form_types_1.png" caption="" width="1024">}}

One can filter form types by their status as `Active` or `Inactive` or see `All` of them. Click the button on the right of each form type to `Activate` or `Deactivate` a specific form type. One can also create a new `Form Type` by clicking the `Create` button.

### Create a new Form Type

{{< figure src="/images/form_types/form_types_2.png" caption="" width="1024">}}

A Form type lets you manage a set of expectation for forms based on this `Form Type`. To create one you have to supply the following options.

| Field | Description |
| --- | --- |
| `Form type tile` | The title for the form type, multi language is provided. |
| `Workflow` | The workflow tied to all forms based on this `Form Type`. |
| `Is there a risk form` | Mark the form type as being a risk form type. |
| `Background color` | Specify the background color for all the forms based on this `Form Type` |
| `Description` | A optional description for a specific form type. |
| `Default template fields` | Allows the specification of fields that should be included when creating a new form based on this form type. |

The `Default template fields` types are the following.

| Field | Description |
| --- | --- |
| `Register on department` | Field that lets you pick the department that the message is to be registered on. |
| `Event occured on` | Provided a component that lets you set the data/time the event associated with the form registration happened. |
| `Choose case handler` | Field that lets you pick what case handler should receive the form entry. |
| `Registered by` | A field that lets the user entering a message pick the person who registered the message. |
| `Registered on behalf of` | A field that lets the user entering a message pick the person they are registering the message on behalf off. |
| `Description field` | A field that lets you provide a description logged as part of the case title, information. |
| `Cost of fault` | A field letting you specify a cost associated with registering a new message. |
| `Priority field` | A field letting you select the priority of the message being registered. |