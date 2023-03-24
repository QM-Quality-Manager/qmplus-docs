---
title: "Administrator/Categories"
description: "A user guide for working with category groups"
lead: "A user guide for working with category groups. We cover how to create and modify category groups."
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
This section deals with managing category groups in the system.

Clicking on the `Administrator/Categories` gives access to the list of category groups.

A Category groups is made of a tree structure of `sub category groups` and `categories`. These elements can be re-organized in whatever order the user sees fit.

> Category groups can be reused across multiple forms allowing you to generate statistics and reports across multiple types of form to compare.

One of the important things to keep in mind is that all `Category Groups` are versioned. This lets you modify a category group without affecting existing form that contain that category group.

## Catgory Group List

{{< figure src="/images/category_groups/category_group_10.png" caption="" width="1024">}}

The category group list view lets us view all the category groups in the system and filter them by several different parameters including the name of the category group and visibility.

{{< figure src="/images/category_groups/category_group_1.png" caption="" width="1024">}}

To access the additional filters click on the filter button and select from the options in the sidebar.

## Create Category Group

{{< figure src="/images/category_groups/category_group_9.png" caption="" width="1024">}}

When creating we have the following available fields.

| Field | Description |
| --- | --- | 
| `Category group title` | The name of the category group. It has multi-language support allowing you to provide translations for other languages you might support in the organization. |
| `Group Type` | The type of category group we are creating. See the description below. |
| `Visibility` | Specify how the category group is visible in the organization. For example setting this to `department` will make the category group only visible for the currently selected department.|
| `Department` | Select the department that this category group will be registered on. Together with `visibility` this controls where the category group is visible |
| `Categories` | This is the main aspect. It allows you to add `sub category groups` as well as `categories` building up a `tree-like` structure of nested information.
| `Reference` | Lets you specify a `document` reference to display with the category group in forms. For example to link to a relevant law. This can also be done for sub category groups and categories added. |

The `Group Type` lets you specify what kind of category group you are creating. The options are.

| Group Type | Description |
| --- | --- |
| `Defining` | A special `Single Choice` category group that is used as a `defining` category group in a form. Allows the end user to select `only one` category as a response. |
| `Single Choice` | Allows the user to select a single `cateogry` when entering data into a form. |
| `Multi Choice` | Allows the user to select multiple `categories` when entering data into a form. |
| `Action Choice` | Allows the user to select a single `category` for an action. This category groups is different from `Single Choice` only in that it's marked as an `action` group. |
| `Number` | Allows the user to enter numeric values for all the categories in the group. This can be used to collect things like currency number or other data. |
| `Risk` | Allows user to enter risk analaysis values for a given attached risk model. |

> In the case of selecting the Group Type `Risk` we will see an additional field in the `Create Category Group` form that lets us select the `Risk Model` this category group will be based on.

{{< figure src="/images/category_groups/category_group_11.png" caption="" width="1024">}}

Click the `Set risk model` button to bring up the sidebar to select the associate risk model.

{{< figure src="/images/category_groups/category_group_12.png" caption="" width="1024">}}

From here you can select the risk model that you want to use with the category group.

{{< figure src="/images/category_groups/category_group_5.png" caption="" width="1024">}}

Finally you can select a `reference document` that you want to add to the category group as a reference.

### Add and Edit Category Group

{{< figure src="/images/category_groups/category_group_8.png" caption="" width="1024">}}

To create a `Sub Category Group` we need to provide a name for the category group. One can add an optional description. 
Finally you can add a reference document for the `Sub Category Group` that will be shown in forms when it renders the sub group.

### Add and Edit Category

{{< figure src="/images/category_groups/category_group_7.png" caption="" width="1024">}}

To add a category to the category group we need to set the following fields.

| Field | Required | Description |
| --- | --- | --- |
| `Category Name` | **X** | Set the name of the category we are adding (support multiple languages). |
| `Description` | | Optional description for the category. |
| `Visibility` | **X** | Specify the default visibility of the category (what department it is visible on). |
| `Department` | **X** | The department from where the category is visible. |
| `Priority` | | The priority to set on the form entry if the category is selected. |
| `Cost` | | The cost set on the form entry if the category is selected. |
| `Reference` | | The optional document reference to show when the category is rendered in a form. |

Finally click the `Save Changes` button to save the new category to the category group.

{{< figure src="/images/category_groups/category_group_3.png" caption="" width="1024">}}

Just as when a new category is created an existing one can be edited.

### Organizing Structure

{{< figure src="/images/category_groups/category_group_6.png" caption="" width="1024">}}

When organizing the category group structure you can drag the item into the order you want.

> Drag categories to the right under a category group to organize it under the sub group.

We can also edit, view category detail or delete categories/sub category groups.

{{< figure src="/images/category_groups/category_group_4.png" caption="" width="1024">}}

This is the view of clicking on the `view category details`.

### References

{{< figure src="/images/category_groups/category_group_2.png" caption="" width="1024">}}

References let you attach links to internal documents that contain relevant information about a given category group, category or sub category group. 
For example links to laws or instructions associated with a given entry.
  