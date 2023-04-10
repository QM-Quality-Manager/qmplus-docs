---
title: "Dashboards"
description: "A user guide for working with dashboards"
lead: "A user guide for working with dashboards. We cover how to create and modify dashboards."
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
This section deals with managing dashboards for the user.

Clicking on the `Dashboards` gives access to the list of the users dashboards.

## Overview

Dashboards are collections of components that you can build to monitor the state of the platform. You can build dashboards for specific objectives or to make specific information available. There are two types of dashboards.

| Type | Description |
| --- | --- |
| `User` | Dashboards the user themselves can build, with components available for them. |
| `User Type` | Read only dashboards created for a specific user types. Used to share fixed information across all users of a specific user type. Can be used to ensure everyone is reporting on the same information. |

### Configure User Type Dashboards

{{< figure src="/images/dashboards/dashboards_22.png" caption="dashboards_22.png" width="1024">}}

To create or modify `User Type` dashboards first navigate to the `User Types` list. Click on one of the `User Types` to bring up the `User Type` and then click on the `Dashboards` tab.

{{< figure src="/images/dashboards/dashboards_23.png" caption="dashboards_22.png" width="1024">}}

Dashboards configured here will show up for the user of that `User Type` when they click on the `Dashboards` menu option.

## Dashboard

{{< figure src="/images/dashboards/dashboards_1.png" caption="dashboards_1.png" width="1024">}}

Above is an example view of a dashboar with some components configured.

{{< figure src="/images/dashboards/dashboards_2.png" caption="dashboards_2.png" width="1024">}}

There are two types of dashboards.

| Type | Description |
| --- | --- |
| `Usertype` | A read-only dashboard specified for the logged in users user type, can be used to ensure uniform reporting of numbers and status. |
| `User created` | A dashboard created by the logged in user. |

{{< figure src="/images/dashboards/dashboards_5.png" caption="dashboards_5.png" width="1024">}}

When clicking on the `Columns` symbol you can adjust the number of colums used to render the dashboard allowing for finer control of the component layout.

{{< figure src="/images/dashboards/dashboards_4.png" caption="dashboards_4.png" width="1024">}}

When clicking the `Configure` button on the dashboard you get access to saved existing components that can be reused. These are of two types.

| Type | Description |
| --- | --- |
| `General` | Components shared across the entire organization and available to all to create, the user must have the permission to create general components to be able to create new components here. |
| `My components` | Components the logged in user has already created and that are only visible for them. | 

## Components

{{< figure src="/images/dashboards/dashboards_3.png" caption="dashboards_3.png" width="1024">}}

There are several components available to add to a dashboard. These can be used to build information dashboards for the end users or yourself.

### Chart

{{< figure src="/images/dashboards/dashboards_8.png" caption="dashboards_8.png" width="1024">}}

Charts lets you create components that visualize data stored in `Q`. Lets look at the options available.

| Option | Description |
| --- | --- |
| `Component name` | Set the name of the component, supports multiple languages. |
| `Case type` | Select the case type for the graph. This is one of `Message`, `Action`, `Document`, `Hearing` and `Audit`. |
| `Display type` | Display type for the graph. This is one of `Line chart`, `Area chart`, `Bar chart` or `Pie chart`. |
| `Stack by` | Enable/Disable stack by field option for the graph. |
| `Stack field` | Select the field to stack by. See table below. |
| `X-axis` | Select the options for the x-axis (x-axis and y-axis can be flipped). |
| `Y-axis` | Select the options for the x-axis (x-axis and y-axis can be flipped). |
| `Period` | Select the time period of the graph data. The fields available will depend on the case type. |
| `Filters` | Add, remove and modify filters to limit the results returned for the graph. |
| `Override expression` | Lets the end user override the query language run against the `Q` backend. |
| `Override visual spec` | Lets the end user override the VegaLite graph definition used to render the graph. |

{{< figure src="/images/dashboards/dashboards_24.png" caption="dashboards_24.png" width="1024">}}

The stack by field available are.

| Field | Description |
| --- | --- |
| `Priority` | Stack by priority level of the case. |
| `Case status` | Stack by the case status of the case. |
| `Department` | Stack by department of the case. |
| `Form` | Stack by the form of the case. |

### Map

{{< figure src="/images/dashboards/dashboards_11.png" caption="dashboards_11.png" width="1024">}}

The map component lets you create a query that will be mapped to a map instance if the message case has associated geo coordinates.

### Table

{{< figure src="/images/dashboards/dashboards_12.png" caption="dashboards_12.png" width="1024">}}

The table component is a list component that shows the results of a specific query. Overlooking the options.

| Option | Description |
| --- | --- |
| `Component name` | Set the name of the component, supports multiple languages. |
| `Case type` | Select the case type for the graph. This is one of `Message`, `Action`, `Document`, `Hearing` and `Audit`. |
| `Columns` | Select the columns visible in the list results. |
| `Count` | Select the number of entries per page in the list. |
| `Period` | Select the date period for the entries in the list. |
| `Filters` | Add, remove and update filters for the query. |
| `Override expression` | Override the current generated expression. |

### Predefined graphs

{{< figure src="/images/dashboards/dashboards_13.png" caption="dashboards_13.png" width="1024">}}

The predefined graphs are pre-made (canned) reports that you can leverage to target specific analytic goals. Lets look at the field of the sidebar.

| Field | Description |
| --- | --- |
| `Component name` | Set the name of the component, supports multiple languages. |
| `Graph type` | Select the predefined graph type, see table below. |
| `Filters` | A set of filter that will vary depending on the predefined graph type the user selects. |
| `Period` | Select data for the report by time period. |
| `Override expression` | Enable/disable the ability to override the expression being sent to `Q`. |

The available predefined graphs are.

| Predefined Graph | Description |
| --- | --- |
| `Cycle and Lead Time Running Average` | Measure the cycle and lead time over a window of running average. See definition of `Cycle` and `Lead` time below. |
| `Case by case status group` | The count of cases over time by cate status group. |
| `Cases by case status` | The count of cases over time by cate status.|
| `Unprocessed vs Open and Closed cases` | Number of cases unprocessed, open and closed over time. |
| `Time spent in case status group by percentile` | Time a case spends in each case status group (setting the percentile, for definition of percentile see below). |
| `Time spent in case status by percentile` | Time a case spends in each case status (setting the percentile, for definition of percentile see below). |
| `Cumulative count of cases by department` | Cummulative count of cases per department. |
| `Cumulative cost of cases by department` | Cummulative cost of cases per department. |

#### Definitions
> Cycle time refers to the average time taken to complete a single unit. The Lead Time refers to the length of time it takes from the date of receipt of an order to the date of delivery.
>
> Percentile, expressed as the percentage of values in a set of data scores that fall below a given value. That is to say that if you set the percentile to 90% and you get a value 100 it means 90% of the results in your data set fall below 100.

#### **Cycle and Lead Time Running Average** Filters
{{< figure src="/images/dashboards/dashboards_25.png" caption="dashboards_25.png" width="1024">}}

The filters available for the `Cycle and Lead Time Running Average` predefined graph type is.

| Field | Description |
| --- | --- |
| `Workflow` | Select the workflow to report on. |
| `Category group` | Select the category group you wish to use to filter the results |
| `Category` | Select the category in the category group to use for filter |
| `Size of the rolling window in days` | The size of the rolling window (we recommend 7 days). |

#### **Case by case status group** Filters
{{< figure src="/images/dashboards/dashboards_26.png" caption="dashboards_26.png" width="1024">}}

The filters available for the `Case by case status group` predefined graph type is.

| Field | Description |
| --- | --- |
| `Workflow` | Select the workflow to report on. |
| `Category group` | Select the category group you wish to use to filter the results |
| `Category` | Select the category in the category group to use for filter |

#### **Cases by case status** Filters
{{< figure src="/images/dashboards/dashboards_27.png" caption="dashboards_27.png" width="1024">}}

The filters available for the `Cases by case status` predefined graph type is.

| Field | Description |
| --- | --- |
| `Workflow` | Select the workflow to report on. |
| `Category group` | Select the category group you wish to use to filter the results |
| `Category` | Select the category in the category group to use for filter |

#### **Unprocessed vs Open and Closed cases** Filters
{{< figure src="/images/dashboards/dashboards_28.png" caption="dashboards_28.png" width="1024">}}

The filters available for the `Unprocessed vs Open and Closed cases` predefined graph type is.

| Field | Description |
| --- | --- |
| `Workflow` | Select the workflow to report on. |
| `Category group` | Select the category group you wish to use to filter the results |
| `Category` | Select the category in the category group to use for filter |

#### **Time spent in case status group by percentile** Filters
{{< figure src="/images/dashboards/dashboards_29.png" caption="dashboards_29.png" width="1024">}}

The filters available for the `Time spent in case status group by percentile` predefined graph type is.

| Field | Description |
| --- | --- |
| `Workflow` | Select the workflow to report on. |
| `Category group` | Select the category group you wish to use to filter the results |
| `Category` | Select the category in the category group to use for filter |
| `Percentile` | The percentile used to calculate the time spent. |

#### **Time spent in case status by percentile** Filters
{{< figure src="/images/dashboards/dashboards_30.png" caption="dashboards_30.png" width="1024">}}

The filters available for the `Time spent in case status by percentile` predefined graph type is.

| Field | Description |
| --- | --- |
| `Workflow` | Select the workflow to report on. |
| `Category group` | Select the category group you wish to use to filter the results |
| `Category` | Select the category in the category group to use for filter |
| `Percentile` | The percentile used to calculate the time spent. |

#### **Cumulative count of cases by department** Filters
{{< figure src="/images/dashboards/dashboards_31.png" caption="dashboards_31.png" width="1024">}}

There are no filters available for the `Cumulative count of cases by department` predefined graph. 

#### **Cumulative cost of cases by department** Filters
{{< figure src="/images/dashboards/dashboards_32.png" caption="dashboards_32.png" width="1024">}}

There are no filters available for the `Cumulative cost of cases by department` predefined graph. 

### My cases

{{< figure src="/images/dashboards/dashboards_14.png" caption="dashboards_14.png" width="1024">}}

The `My cases` component provides you with information related to the current logged in user. There are three tabs.

| Tab | Description |
| --- | --- |
| `Messages I reported` | Messages I entered into the platform. |
| `My cases as a case handler` | All the cases I'm assigned to as a case handler. |
| `My tasks` | All my assigned tasks on cases. |

### My activities

{{< figure src="/images/dashboards/dashboards_15.png" caption="dashboards_15.png" width="1024">}}

The `My activites` component shows you all upcoming activities the current logged in user is associated with. The user can directly acess any given activity by clicking the link for each row.

### Escalated Cases

{{< figure src="/images/dashboards/dashboards_16.png" caption="dashboards_16.png" width="1024">}}

The `Esclated cases` show all the cases that have been escalated by the system in the period specified in the filters allowing the logged in user to view and operate on the escalated cases.

### Document updates

{{< figure src="/images/dashboards/dashboards_17.png" caption="dashboards_17.png" width="1024">}}

The `Document updates` component lets the logged in user see what documents have been updated in the period specifiec by the filters in the component settings. For example that might be to see all updated documents in the last 7 days.

### Favorite documents

{{< figure src="/images/dashboards/dashboards_19.png" caption="dashboards_19.png" width="1024">}}

The `Favorite documents` component shows all the documents favoritted by the currently logged in user.

### Inline document viewer

{{< figure src="/images/dashboards/dashboards_20.png" caption="dashboards_20.png" width="1024">}}

The `Inline document viewer` component lets you embed a document directly in the dashboard as viewable. The following types of document types are supported.

| Type | Description |
| --- | --- |
| `Text Document` | A HTML like document viewed in the component. |
| `Process chart` | A Process chart document rendered in the component. |
| `Richtext` | A read-only rich text document stored in `Q`. |
| `Spreadsheet` | A read-only spreadsheet stored in `Q`. |

> All `Inline document` documents are `READ ONLY` and cannot be edited.