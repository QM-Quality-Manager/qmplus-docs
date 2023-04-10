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
weight: 9
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

> One can also use the `Upload` button to upload files instead of dragging and dropping files.

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

### Create a new **Text document**

{{< figure src="/images/document_manager/document_manager_24.png" caption="document_manager_24.png" width="1024">}}

The `Text document` has a `Content` tab that allows us to edit the document.

{{< figure src="/images/document_manager/document_manager_23.png" caption="document_manager_23.png" width="1024">}}

The content editor lets us edit HTML like content with a basic set of formatting options.

### Create a new **Link document**

{{< figure src="/images/document_manager/document_manager_25.png" caption="document_manager_25.png" width="1024">}}

The special area for a `Link` document is udner the `Title and description` tab where one can set the external link associated with this document.

> Its possible to provide multiple links in the same document case one for each language.

### Create a new **Process chart document**

{{< figure src="/images/document_manager/document_manager_32.png" caption="document_manager_32.png" width="1024">}}

The process chart tool lets you create simple process charts that you can store as documents, embed in dashboards. You can also link to other documents making clickable maps.

### Create a new **Richtext document**

{{< figure src="/images/document_manager/document_manager_33.png" caption="document_manager_33.png" width="1024">}}

A more Microsoft Word like interface for richer documents.

### Create a new **Spreadsheet document**

A basic Excel like interface for richer spreadsheets.

{{< figure src="/images/document_manager/document_manager_34.png" caption="document_manager_34.png" width="1024">}}

## Editing an existing Document

{{< figure src="/images/document_manager/document_manager_42.png" caption="document_manager_42.png" width="1024">}}

When working with documents it's important to understand that there are two main states documents exist in.

| State | Description |
| --- | --- |
| `Draft` | When you are working on a document and making changes then clicking the `Save` button we save a draft version that is not visible to end users. To make the changes visible one has to explicitly publish the document. |
| `Published` | A published document is a document visible to end users. This lets you make changes to a document in private and only publish when ready. |

A document can also be marked as a `Template` allowing you to use this document as a basis for a new document. When creating a new document from a `Template` it will be created from the latest `Published` version.

> Click the `New Version` button to create a new version. This button is only enabled when the current document is in a `closed` state and will reset the workflow to the start again, letting you start another version of the document.

## Copy Document to Another Directory

{{< figure src="/images/document_manager/document_manager_6.png" caption="document_manager_6.png" width="1024">}}

Select a document. Once a document is selected the toolbar changes allowing you to click the `Copy to` button.

{{< figure src="/images/document_manager/document_manager_7.png" caption="document_manager_7.png" width="1024">}}

Select a target directory and click the `Select` button to make a copy of the document into another folder.

## Move Document to Another Directory

{{< figure src="/images/document_manager/document_manager_8.png" caption="document_manager_8.png" width="1024">}}

To move a document to a new folder, click on the `Send to` button and then select a destination folder for the file.

## Import Documents from SharePoint

{{< figure src="/images/document_manager/document_manager_10.png" caption="document_manager_10.png" width="1024">}}

If `Sharepoint` is enabled as an integration point for your organization you'll have access to an `Import` button letting you import documents from configured `Sharepoint` shares.

{{< figure src="/images/document_manager/document_manager_36.png" caption="document_manager_36.png" width="1024">}}

When importing documents from `Sharepoint` we need to enter several fields outlined below.

| Field | Description |
| --- | --- |
| `Site` | Select the `Sharepoint` site (share) to import documents from. |
| `Documents` | Brings up the document navigator allowing you to select the `Sharepoint` documents to import. |
| `Import to` | Set the visibility, department and document folder for all the imported documents. |
| `Workflow` | Set the associated document workflow to use with all the imported documents. |
| `Synchronize updates` | Specify if `Q` will intermittently query `Sharepoint` to check if there are new versions of the documents and import the updated documents automatically. |

Clicking the `Document` button will bring up a file manager allowing you to select documents from the specified `Sharepoint Site`.

{{< figure src="/images/document_manager/document_manager_37.png" caption="document_manager_37.png" width="1024">}}

Once you've selected the files you wish to import, click the `Confirm` button to go back to the `Import from Sharepoint` dialog.

{{< figure src="/images/document_manager/document_manager_38.png" caption="document_manager_38.png" width="1024">}}

To finish the import click the `Import` button.

{{< figure src="/images/document_manager/document_manager_31.png" caption="document_manager_31.png" width="1024">}}

As we can see the imported files from `Sharepoint` have a `Sharepoint logo` and symbol signaling that this as import from `Sharepoint`.

## Export Documents from SharePoint

{{< figure src="/images/document_manager/document_manager_39.png" caption="document_manager_39.png" width="1024">}}

Select one or more files and if your organization has `Sharepoint` enabled the user wille see an `Export` button allowing them to export the selected documents to `Sharepoint`.

{{< figure src="/images/document_manager/document_manager_40.png" caption="document_manager_40.png" width="1024">}}

When exporting documents from `Sharepoint` we need to enter several fields outlined below.

| Field | Description |
| --- | --- |
| `Site` | Select the `Sharepoint` site (share) to export documents to. |
| `Documents` | The list of documents being exported to Sharepoint. |
| `Document folder` | The target Sharepoint folder for the exported documents. |
| `Synchronize updates` | When checked `Q` will updated documents to Sharepoint automatically, keeping them in sync. |

Finally click on the `Export` button to finalize the export of documents to `Sharepoint`.

{{< figure src="/images/document_manager/document_manager_41.png" caption="document_manager_41.png" width="1024">}}

Once you've exported the documents they will be visible in the document manager with a `Sharepoint` symbol and an `Export` symbol.
