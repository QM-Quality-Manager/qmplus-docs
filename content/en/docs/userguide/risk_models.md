---
title: "Administrator/Riskmodels"
description: "A user guide for working with risk models"
lead: "A user guide for working with risk models. We cover how to create and modify risk models."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 12
toc: true
---
This section deals with managing risk models in the system.

Clicking on the `Administrator/Riskmodels` gives access to the list of risk models.

## Risk models List

{{< zoomableImage src="/images/risk_models/risk_model_1.png" caption="List of Risk models" width="1600" height="600px">}}

The list of risk models can be filtered by `active/deactive or all`. You can also `activate / deactive` risk models making them not visible when creating new category groups.
Finally clicking the `Create` button will allow us to create a new `Risk Model`.

## Create new Risk Model

### General Pages

{{< zoomableImage src="/images/risk_models/risk_model_2.png" caption="General page" width="1600" height="600px">}}

To create a new `Risk Model` we need to specify a name for the risk model (it supports multiple languages). One can also add an optional description for the model.

### Building the Risk Model

{{< zoomableImage src="/images/risk_models/risk_model_3.png" caption="Building a Risk model" width="1600" height="600px">}}

A risk model is composed of dimensions that contain scales with values used to calculate a final score. 

> For example, you might have a `Likelihood` scale as well as an `Impact` scale, where each scale in each dimension has an associated value.

When entering a risk value, the user will choose one value from each dimension, and the platform will then calculate a corresponding risk value dependent on the formula associated with the risk model.

As you add scales to the dimensions, you can see the preview of the risk model on the left. To define colors based on the calculated values in the risk matrix, we can provide ranges with associated colors by adding and modifying the color range levels at the bottom right corner.

{{< zoomableImage src="/images/risk_models/risk_model_4.png" caption="Basic risk model example" width="1600" height="600px">}}

This model shows a complete basic risk model with associated dimensions, scales, and color ranges.

{{< zoomableImage src="/images/risk_models/risk_model_6.png" caption="Adding a new scale or dimension" width="1600" height="600px">}}

When adding or editing a new `scale` to a `dimension`, we can provide a name, description, and value for the scale.

### Versioning of Risk Model

{{< zoomableImage src="/images/risk_models/risk_model_5.png" caption="Risk model versions" width="1600" height="600px">}}

All risk models are versioned. This is done so that changes to a risk model do not impact existing forms.