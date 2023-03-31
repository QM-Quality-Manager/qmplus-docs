---
title: "Administrator/Questionnaires"
description: "A user guide for working with questionnaires"
lead: "A user guide for working with questionnaires. We cover how to create and modify questionnaires."
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
This section deals with managing questionnaires in the system.

Clicking on the `Administrator/Questionnaires` gives access to the list of questionnaires.

## Questionnaires List

{{< figure src="/images/questionnaires/questionnaires_1.png" caption="" width="1024">}}

Questionnaires are used to create long questionnairs and check lists that can span either a single page or multiple pages.

You can filter between `Active`, `Deactive` or `All` status, search by title and if the questionnaire is published or not.

## Create Questionnaire

### General Tab

{{< figure src="/images/questionnaires/questionnaires_2.png" caption="" width="1024">}}

Creating a questionnaire requires the following field.

| Field | Description |
| --- | --- |
| `Title` | Title of the questionnire, support multiple languages. |
| `Description` | Optional description for the questionnaire. |
| `Questionnaire display type` | How to render the questionnaire (Single Page or Multiple Pages). |
| `Visiblity` | Visiblity of the questionnaire. |
| `Department` | On what department the questionnaire is located. |
| `Reference` | One or more document references attached to the questionnaire. |
| `Tags` | Add tags to questionnaire to identify the questionnaire. |

As you can see from the image we can preview the current questionnaire.

> Until you click the `Publish` button all changes to the questionnaire are private. Once the `Publish` button is clicked it will be visible to add to activities.

### Questionnaire Layout

{{< figure src="/images/questionnaires/questionnaires_8.png" caption="" width="1024">}}

The Questionnaire Builder has some core concepts to wrap ones head around. A questionnaire is a collection of of one or more pages, where each page has one or more columns of components. The preview button lets you test the questionniare during development. Clicking the save button will save a new version of the Questionnaire and once ready you can click `Publish` to release the new Questionnaire to be used.

> All Questionnaire entries are tied to a specific Questionnaire Version meaning old data is preserved correctly against the a previous version of a Questionnaire.

{{< figure src="/images/questionnaires/questionnaires_4.png" caption="" width="1024">}}

The available components are as follows.

| Component | Description |
| --- | --- |
| `Text` | |
| `Image` ||
| `Single choice` ||
| `Multi choice` ||
| `Ranking` ||
| `Integer` ||
| `Decimal` ||
| `Currency` ||
| `Number in range` ||
| `One-line text field` ||
| `Multiline text field` ||
| `Risk` ||


{{< figure src="/images/questionnaires/questionnaires_9.png" caption="" width="1024">}}


{{< figure src="/images/questionnaires/questionnaires_5.png" caption="" width="1024">}}
{{< figure src="/images/questionnaires/questionnaires_6.png" caption="" width="1024">}}
{{< figure src="/images/questionnaires/questionnaires_7.png" caption="" width="1024">}}
