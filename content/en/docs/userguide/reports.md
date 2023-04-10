---
title: "Reports"
description: "A user guide for working with reports"
lead: "A user guide for working with reports."
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
This section deals with creating and updating `reports`.

Clicking on the `reports` gives access to the list of the reports available.

Reports lets you build reports of data in `Q` than can be used to monitor and report on statistics of the data collected.

There are two categories of reports in the system.

| Type | Description |
| --- | --- |
| `Normal Reports` | Normal reports made up of graphs and predefined canned graphs. |
| `Risk Reports` | Risk reports made up risk report elements. |

> All reports update when you change the `department` in the navigator allowing you to drill down in the data and compare data across departments.

## Case Report List

{{< figure src="/images/reports/reports_1.png" caption="reports_1.png" width="1024">}}

Clicking the `Case Report` link brings you to the list of `Case Reports` in the system.

### Preview
{{< figure src="/images/reports/reports_2.png" caption="reports_2.png" width="1024">}}

Clicking on the `Preview` (eye symbol) in the list we bring up a preview of the report in read-only mode.

{{< figure src="/images/reports/reports_15.png" caption="reports_15.png" width="1024">}}

Clicking on the `Zoom into results` icon will bring up the complete list of all the data associated with the graph component so you can explore the cases that make up the data.

{{< figure src="/images/reports/reports_16.png" caption="reports_16.png" width="1024">}}

Clickin on one of the segements of the bar graph will zoom in and show only the cases that make up that bar.

### Editing Report

{{< figure src="/images/reports/reports_3.png" caption="reports_3.png" width="1024">}}

When editing or creating a new report, you need to provide a `Report name` before saving. One can also set a description for the report as well as add tags to group reports by keywords.

Adding elements to the graph lets you build a graph representing multiple analytic components.

There are two main report types.

| Type | Description |
| --- | --- |
| `General chart` | A general report element chart that.  |
| `Predefined charts` | Pre-defined reports allowing for specific report elements. | 

{{< figure src="/images/reports/reports_4.png" caption="reports_4.png" width="1024">}}

When editing or adding a new Element to a report you have the following options for a `General Chart`.

| Option | Description |
| --- | --- |
| `Edit filters` | Edit the filters used to limit the data used for the graph. |
| `Report Type` | Let the user switch between a `General chart` or `Predefined chart`. |
| `Case Type` | Choose the type of case to use gor the graph. `Message`, `Action` or `Document`. |
| `Group by` | Select the field to group by. |
| `Stack by` | Select a field to stack by. `Status`, `Priority`, `Category`, `Category group` or `Form`.  The available field will depend on the `Case type` selected. |

{{< figure src="/images/reports/reports_6.png" caption="reports_6.png" width="1024">}}

Editing the filters will bring up a sidebar where the user can modify the filters used to slice and dice the data for the graph.

{{< figure src="/images/reports/reports_7.png" caption="reports_7.png" width="1024">}}

If you select the `Predefined charts` option from the `Report Type` dropdown you will se a form like above. Depending on the type of `Predefined chart` the user will have options available to tweak the results of the report element. The available `Predefined charts` are.

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

## Risk Report List

{{< figure src="/images/reports/reports_9.png" caption="reports_9.png" width="1024">}}

Clicking the `Risk Report` link brings you to the list of `Risk Reports` in the system. Risk reports are reports that report against a specified `Risk model` allowing us to drill into `Messages` that have risk category groups associated with them.

Click on the `Preview` button of a `Risk Report` will bring up the preview of the report.

### Preview

{{< figure src="/images/reports/reports_8.png" caption="reports_8.png" width="1024">}}

Click on the boxes in the rendered risk model takes you directly to the cases associated with the factors of the risk model allowing you to investigate the associated cases with specific report.

### Editing Report

{{< figure src="/images/reports/reports_11.png" caption="reports_11.png" width="1024">}}

When editing or creating a new report, you need to provide a `Report name` before saving. One can also set a description for the report as well as add tags to group reports by keywords.

Adding elements to the graph lets you build a graph representing multiple risk analysis components.

{{< figure src="/images/reports/reports_13.png" caption="reports_13.png" width="1024">}}

Looking at the add `Risk element` interface we can see the following options when the `Graph / Risk model toggle` is set to `Risk model`.

| Option | Description |
| --- | --- |
| `Graph / Risk model toggle` | Toggle between graph or risk model view. |
| `Edit filters` | Adjust the filters to filter down the results. |
| `Risk model` | Select the risk model to use for the graph. |

{{< figure src="/images/reports/reports_14.png" caption="reports_14.png" width="1024">}}

Looking at the add `Risk element` interface we can see the following options when the `Graph / Risk model toggle` is set to `Graph`.

| Option | Description |
| --- | --- |
| `Graph / Risk model toggle` | Toggle between graph or risk model view. |
| `Edit filters` | Adjust the filters to filter down the results. |
| `Risk model` | Select the risk model to use for the graph. |
| `Group by` | Group by field. `Department`, `Status`, `Priority`, `Category`, `Category group`, `Form`, `Year`, `Month`, `Date` or `Risk level`. |
| `Stack by` | Stack by the following field. `Status`, `Priority`, `Category`, `Category group`, `Form` or `Risk level`. |
| `Display type` | Select the display type. Either `Cases count` or `Cost of fault`. |
