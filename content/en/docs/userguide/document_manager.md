---
title: "Administrator/Document Administrator"
description: "A user guide for working with the document administrator"
lead: "A user guide for working with the document administrator. We cover how to create, update and manage documents."
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

Clicking on the `Administrator/Document Administrator` gives access to the document manager.

## Document Manager

{{< figure src="/images/document_manager/document_manager_1.png" caption="document_manager_1.png" width="1024">}}

The document manager is the heart of the document management system. It allows for organizing documents, creating new ones, upload existing ones, edit or deactivee existing ones.

{{< figure src="/images/document_manager/document_manager_3.png" caption="document_manager_3.png" width="1024">}}

As we can see from the filter we can slice and dice the documents visible in the document manager to zero in on a specific document.

> Remember that all documents are associated with departments. That is to say that the view of documents in the manager will change as you modify the visiblity and what department you are looking at. For example, to see all documents in the child departments you can choose `All` from `Document folders visiblity`.

## Create a new Folder

{{< figure src="/images/document_manager/document_manager_4.png" caption="document_manager_4.png" width="1024">}}

To create a new folder provide the name of the folder in multiple languages if supported.

## Document Folder View

{{< figure src="/images/document_manager/document_manager_5.png" caption="document_manager_5.png" width="1024">}}

When one selects a document folder view we have the following options.

| Option | Description |
| --- | --- |
| `New Folder` | Create a new folder underneath the currently selected document on the left side. |
| `New Document` | Create a new document in this document folder. |
| `Refresh` | Refresh the current document folder view. |
| `Rename` | Rename the current document folder. |
| `Upload` | Upload a document into this document folder. |

> One can also upload documents by dragging them and dropping them into the document folder directly.

{{< figure src="/images/document_manager/document_manager_18.png" caption="Upload form after dropping file on the document folder" width="1024">}}

When one or more files are dropped on the document folder upload dialog pops up with the following options.

| Options | Description |
| --- | --- |
| `Files` | Ths list of documents that will be uploaded when clicking the `Upload` button. |
| `Visibility` | Set the visibility of the documents uploaded. |
| `Workflow` | Select the workflow all the uploaded documents will be associated with. | 

## Create a new Document

{{< figure src="/images/document_manager/document_manager_19.png" caption="Create document view" width="1024">}}

When clicking the `New Document` button the new document dialog is brought up with the following options.

| Option | Description |
| --- | --- |
| `Document title` | The title of the new document, supports multiple languages. |
| `Document position` | The list of document positions (visibility and department) associated with the new document. |
| `Document type` | The type of document, see the table below. |
| `Workflow` | Select the associated workflow with the new document we are creating. |
| `Available document templates` | Optionally select a template to base the new document on. |
| `Description` | Optional description for the new document. |
| `Assigned permissions` | Assign permissions to limit access to the document. |
| `Tags` | Add tags to group the document with other documents using keywords. |

The supported document types are.

| Document Type | Description |
| --- | --- |
| `Link` | A document representing an external link from Q. |
| `File` | An uploaded file such as a word document, pdf, image or video. |
| `Text document` | A simple html text document (with simple formatting) stored in the system. |
| `Process chart` | A process diagram (Visio style light) to draw process charts meant to be used in the application. |
| `Richtext` | A rich wordprocessor document (microsoft word light) allowing for more complex document entry.|
| `Spreadsheet` | A basic spreadsheet document, with a minimum set of functionality. |

### Create a new `File document`

{{< figure src="/images/document_manager/document_manager_20.png" caption="document_manager_20.png" width="1024">}}

The main aspects special to the document case.

| Tab | Description |
| --- | --- |
| `Document data` | Contains where the document is located and allows adding additional data elements if more information needs to be captured for the document case. |
| `Title and description` | Title and description of the document case. |
| `Stored Files` | Files stored for this document case. |
| `Versions` | All the versions of this document case. |

{{< figure src="/images/document_manager/document_manager_21.png" caption="document_manager_21.png" width="1024">}}

On the `Title and description` tab we can change the `title`, `description`for all the languages. You can also upload new versions of the file or new files for different languages.

> All documents in Q support multiple languages allowing you to keep all language versions of a procedure bundled into one managable case. For example you might have production process that needs to be available in Norwegian and English.

### Create a new `Text document`

{{< figure src="/images/document_manager/document_manager_24.png" caption="document_manager_24.png" width="1024">}}

The `Text document` has a `Content` tab that allows us to edit the document.

{{< figure src="/images/document_manager/document_manager_23.png" caption="document_manager_23.png" width="1024">}}

The content editor lets us edit HTML like content with a basic set of formatting options.

### Create a new `Link document`

{{< figure src="/images/document_manager/document_manager_25.png" caption="document_manager_25.png" width="1024">}}

The special area for a `Link` document is udner the `Title and description` tab where one can set the external link associated with this document.

> Its possible to provide multiple links in the same document case one for each language.

### Create a new `Process chart document`

### Create a new `Richtext document`

### Create a new `Spreadsheet document`

{{< figure src="/images/document_manager/document_manager_6.png" caption="document_manager_6.png" width="1024">}}
{{< figure src="/images/document_manager/document_manager_7.png" caption="document_manager_7.png" width="1024">}}
{{< figure src="/images/document_manager/document_manager_8.png" caption="document_manager_8.png" width="1024">}}
{{< figure src="/images/document_manager/document_manager_9.png" caption="document_manager_9.png" width="1024">}}
{{< figure src="/images/document_manager/document_manager_10.png" caption="document_manager_10.png" width="1024">}}
{{< figure src="/images/document_manager/document_manager_12.png" caption="document_manager_12.png" width="1024">}}
{{< figure src="/images/document_manager/document_manager_13.png" caption="document_manager_13.png" width="1024">}}
{{< figure src="/images/document_manager/document_manager_15.png" caption="document_manager_15.png" width="1024">}}
