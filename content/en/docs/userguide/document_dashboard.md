---
title: "Administrator/Document Dashboards"
description: "A user guide for working with the document dashboards"
lead: "A user guide for working with the document dashboards. We cover how to create, update and manage documents dashboards."
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
This section deals with managing documents in the system.

Clicking on the `Administrator/Document Dashboards` gives access to the document manager.

Document dashboards are how you organize the publishing of documents for end users to see. They let you pick from your document library (as represented by the document manager) and build structure components or search components to show the documents to users.

## List of Document Dashboards

{{< figure src="/images/document_dashboards/document_dashboards_1.png" caption="document_dashboards_1.png" width="1024">}}

The list of dashbaords show you basic information about the dashboards, including title, creation date, department the dashboard is registered on, the visibility and position in the list of dashboards the user will see. You can also delete dashboards from here.

## Create a new Document Dashboard

{{< figure src="/images/document_dashboards/document_dashboards_16.png" caption="document_dashboards_16.png" width="1024">}}

To create a new `Document Dashboard` we need to fill in the following fields.

| Field | Description |
| --- | --- |
| `Document dashboard title` | The name of the dashboard title, supports multiple languages. |
| `Visbility` | Visibility of the document dashboard. |
| `Department` | The department the dashboard is located on. |
| `Position` | The position in the list of dashboards the user can see when they click the `Documents` option. |

After filling in and selection options, click on the `Save` button to create an empty `Document dashboard`, letting us build components for it.

When building new dashboards or editing existing one there are three tabs that we care about.

| Tab | Description |
| --- | --- |
| `General` | The general settings for the `document dashboard`. |
| `Components` | A list of components added to the dashboard including their visiblity settings, will show all dashboard components independently of their visibility and department settings. |
| `Preview` | A preview/builder for components. This component updates when you change the currently selected department letting you see how the dashboard looks depending on the selected department. |

## Preview

{{< figure src="/images/document_dashboards/document_dashboards_4.png" caption="document_dashboards_4.png" width="1024">}}

The `Preview` tab is the tab we use to configure the look and content of the document dashboard in question. The options available are.

| Option | Description |
| --- | --- |
| `Number of column` | Allows you to specify the number of columns shown in the dashboard. |
| `Configure` | Configure the dashboard, including adding existing components or creating new ones |
| `Add component` | Quick add a new structure or search component. |

### Preview > Configure

{{< figure src="/images/document_dashboards/document_dashboards_5.png" caption="document_dashboards_5.png" width="1024">}}

The configure button will bring up the `Configure` sidebar allowing access to adding configurations from either the `General` components list or the users `My components` list.

> To add components to the `General` components list you have to have the permission to operate on the general components. Otherwise you can only selecte existing components from the `General` components list.

Each of the components can be added by sliding the toggle on the right side to end, which will add the component to the current dashboard.

If there are many components in the list you can filter them by clicking on the search icon and narrowing the list searching by name of the component.

Clicking on `Add Component` will let you add a new `Structure` or `List Search` component. See the information about creating new components under the `Add Component` section.

### Preview > Add Component

{{< figure src="/images/document_dashboards/document_dashboards_6.png" caption="document_dashboards_6.png" width="1024">}}

When clicking the `Add Component` button you can pick between the `Static Structure` and `List` options.

| Option | Description |
| --- | --- |
| `Static Structure` | A static structure of documents letting the user build the structure manually by adding a directory and file structure defined by the user. |
| `List` | A list of documents based on a search. Lets the user use tags and other restrictions to group documents into a list. This creates dynamic views that can help organize documents automatically as new documents matching the query will show up automatically. |

### Preview > Add Structure Component

{{< figure src="/images/document_dashboards/document_dashboards_10.png" caption="document_dashboards_10.png" 
width="1024">}}

The structure components lets you build completely custom directory and file components organizing the structure as needed. The field options are.

| Option | Description |
| --- | --- |
| `Component name` | The name of the dashboard component. |
| `Color` | The color of the dashboard component. |
| `Type` | The type of the component, one can switch between the structured component and list. |
| `Visibility` | The visibility of the component. |
| `Department` | The department of the component. |
| `Static structure > New folder` | Add a new folder to the structure. |
| `Static structure > Add document` | Add a new document to the structure. |

Clicking on the `Add document` icon will bring up a sidebar, that lets you browse the document manager files available and add the documents.

{{< figure src="/images/document_dashboards/document_dashboards_11.png" caption="document_dashboards_11.png" width="1024">}}

You can browse the document folders, filter and search for files, then select multiple files to add in one go. Once you are ready click the `Select N documents` button to add them to your `Structure` component.

Clicking on the `Add folder` icon will bring up a sidebar allowing you to create a new document folder and adding it to your `Structure` component.

{{< figure src="/images/document_dashboards/document_dashboards_12.png" caption="document_dashboards_12.png" width="1024">}}

Enter the name of the folde (supports multiple languages), then click the `Save changes` button to add the folder to your structure.

{{< figure src="/images/document_dashboards/document_dashboards_13.png" caption="document_dashboards_13.png" width="1024">}}

Above is an image of a `Structured` component containing a `Folder` and a couple of `Documents`. You can drag around the order of the itmes. To move a document under a `Folder` drag it from left to right under a folder and it will be attached underneath that `Folder`. Documents and Folders can also be removed from the structured component.

### Preview > Add List Component

{{< figure src="/images/document_dashboards/document_dashboards_8.png" caption="document_dashboards_8.png" width="1024">}}

A list component is a component that runs a `Search` for documents and displays any matching documents. The options for the componet are.

| Option | Description |
| --- | --- |
| `Sorting` | Defined the sort order of the documents in the list. |
| `Filters` | Add filters to limit the documents appearing in the list. |

For sorting the list there is the following options.

| Sort Option | Description |
| --- | --- |
| `Registered On` | Sort by the `Registered On` date of the document. |
| `Changed On` | Sort by the `Changed On` date of the document. |
| `Type` | Sort by the document type. |
| `Name` | Sort by the document name. |

The sort order can be in `Decending` or `Ascending` order.

For filtering the list there is the following options.

| Filter Option | Description |
| --- | --- |
| `Period` | The period of the document by either `Registered on` or `Changed on`. |
| `Search` | A text search on the name of the documents. |
| `Tags` | A set of tags separated by comma. |
| `Case status` | Documents with a specific case status. |
| `Document folder` | Filter by a specific document folder in the document manager. |

### Preview result

{{< figure src="/images/document_dashboards/document_dashboards_14.png" caption="document_dashboards_14.png" width="1024">}}

Above is an example of a `Dashboard` with a `List` and `Structure` component. As we can see we can `Minimize/Maximize` the component, as well as resize and move the component on the dashboard. Existing component can also be re-configured as well as removed from the `Dashboard`.

