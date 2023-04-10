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
weight: 15
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

{{< figure src="/images/questionnaires/questionnaires_7.png" caption="" width="1024">}}

References can be added to documents stored in `Q` to add context to a Questionnaire or relevant documents.

## Questionnaire Layout

{{< figure src="/images/questionnaires/questionnaires_8.png" caption="" width="1024">}}

The Questionnaire Builder has some core concepts to wrap ones head around. A questionnaire is a collection of of one or more pages, where each page has one or more columns of components. The preview button lets you test the questionniare during development. Clicking the save button will save a new version of the Questionnaire and once ready you can click `Publish` to release the new Questionnaire to be used.

> All Questionnaire entries are tied to a specific Questionnaire Version meaning old data is preserved correctly against the a previous version of a Questionnaire.

{{< figure src="/images/questionnaires/questionnaires_4.png" caption="" width="1024">}}

The available components are as follows.

| Component | Description |
| --- | --- |
| `Text` | A text description field to enter text information on the questionnaire. |
| `Image` | Allows adding an image to the questionnaire, can be used to show information. |
| `Single choice` | Create a question with answers, allowing the end user to choose one. |
| `Multi choice` | Create a question with answers, allowing the end user to choose multiple ones. |
| `Ranking` | Create a question with answers, allowing the end user to drag and drop them in the order of ranking. | 
| `Integer` | A field that lets you specify a whole number. |
| `Decimal` | A field that lets you specify a decimal number. |
| `Currency` | A field that lets you specify a currency number. |
| `Number in range` | A field that lets you specify a start and end value and the step size for the slider. |
| `One-line text field` | A single line text field. |
| `Multiline text field` | A multiple line text field. |
| `Risk` | A Risk category group. |

> Components can be resized horizontally and moved around. Depending on the number of columns you define you can organize the components side by side.

### Page Settings

{{< figure src="/images/questionnaires/questionnaires_9.png" caption="" width="1024">}}

The page settings allow you change the page title as well as description. You can also add references to documents from Q as well as tags.

### Text
{{< figure src="/images/questionnaires/questionnaires_12.png" caption="" width="1024">}}

A text field that lets you specify some read-only text for the questionnaire. Can be used for instructions related to a field or additional information.

### Image
{{< figure src="/images/questionnaires/questionnaires_13.png" caption="" width="1024">}}

Add a read-only image to the questionnaire to show instructions or additional information related to a question.

### Single choice
{{< figure src="/images/questionnaires/questionnaires_14.png" caption="" width="1024">}}

Create a question/answer combination that lets the person entering a questionnaire select one single option.

### Multi choice 
{{< figure src="/images/questionnaires/questionnaires_15.png" caption="" width="1024">}}

Create a question/answer combination that lets the person entering a questionnaire select multipl options.

### Ranking
{{< figure src="/images/questionnaires/questionnaires_16.png" caption="" width="1024">}}

Create a question/answer combination that lets the person entering a questionnaire rank the options from top to bottom.

### Integer
{{< figure src="/images/questionnaires/questionnaires_17.png" caption="" width="1024">}}

Create a whole number entry field for you questionnaire (Age of a user, street number).

### Decimal
{{< figure src="/images/questionnaires/questionnaires_18.png" caption="" width="1024">}}

Create a decimal number entry field for you questionnaire (for example percentage 5,5).

### Currency
{{< figure src="/images/questionnaires/questionnaires_19.png" caption="" width="1024">}}

Create a currency number entry field for you questionnaire (for example cost 2000,20).

### Number in range
{{< figure src="/images/questionnaires/questionnaires_20.png" caption="" width="1024">}}

Create a numeric range with a minimum and maximum and a step size. For example a age slider with a minimumm og 1 and maximum of 120 years where the step size is 5 will let you drag the slider in intervals of 5 years.

### One-line text field
{{< figure src="/images/questionnaires/questionnaires_21.png" caption="" width="1024">}}

A single text input field. For example to capture a users last name.

### Multiline text field
{{< figure src="/images/questionnaires/questionnaires_22.png" caption="" width="1024">}}

A multiple lines text input field to capture more information in text.

### Risk
{{< figure src="/images/questionnaires/questionnaires_23.png" caption="" width="1024">}}

Select a risk model category group to add to the questionnaire.

{{< figure src="/images/questionnaires/questionnaires_24.png" caption="" width="1024">}}

Lets you perform a risk analaysis evaluation in the questionnaire.

## Questionnaire Versions

{{< figure src="/images/questionnaires/questionnaires_5.png" caption="" width="1024">}}

Everytime you save the questionnaire we create a new version. Once you are ready you can click the `Publish` button to make the current version available to add to Activities.

## Preview Questionnaire

{{< figure src="/images/questionnaires/questionnaires_6.png" caption="" width="1024">}}

Vi can preview the Questionniare seting how it's rendered by clicking the `Preview (eye)` button. You can interact with the elements but not save it.

