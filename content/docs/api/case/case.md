---
title: "Case"
description: "Covering the case handling API."
lead: "Covers use of case API."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu: 
  docs:
    parent: "case"
weight: 130
toc: true
---

### Overview

In this chapter we will look at how we can retrieve the case, modify it and also retrieve history. Its important to understand that a case is associated with an entity and workflow. The types of entities supported are.

| Entity | Description |
| --- | --- |
| `MESSAGE` | A case attached to a specific registered message |
| `ACTION` | A case representing an Action to resolve one or more messages |
| `DOCUMENT` | A case representing a document and its associated process |
| `AUDIT` | A case representing an audit process of one or more documents |
| `HEARING` | A case representing a hearing process for a given document |