---
title: "Administrator/User Permissions"
description: "A user guide for working with user permissions"
lead: "A user guide for working with user permissions. We cover how to create and modify user permissions."
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
This section deals with managing user permissions in the system.

Clicking on the `Administrator/User Permissions` gives access to the list of all available permissions.

There are two types of permissions in the system.

| Type | Description |
| --- | --- |
| `System` | System permissions are permissions that control the access to sections or actions in the application itself and provided from the application. These might be permissions that let you administer users for example or view reports. These cannot be customized by the user and as new functionality is added might expand. |
| `Custom` | Custom permissions are permissions that the user can create that can be used to tag content such as documents, or limit access to things like departments. For example you might have a `confidential` document that you only want two people to access to. In this case you could make a `confidential document` custom permission and assign it to the document as well as the two users that you want to have access. The lack of the permission will block the user from being able to access the document. |

[See all available System Permissions]({{< ref "/content/en/docs/references/permissions.md" >}} "System Permissions")

## Permissions List

### System Permissions

{{< figure src="/images/user_permissions/user_permissions_1.png" caption="System permissions list" width="1024">}}

In this image we can see the list of `System Permissions`. These permissions can be filtered to search for specific permissions. `System Permissions` cannot be modified or deleted and represents all the `Application Level Permissions` availble for your account. Depending on the options you have contract there might be more or less permissions availble.

A complete list of `System Permissions` can be found here.

### Custom Permissions

{{< figure src="/images/user_permissions/user_permissions_2.png" caption="Custom permissions list" width="1024">}}

Custom permissions are permissions that the user can create that can be used to tag content such as documents, or limit access to things like departments. For example you might have a `confidential` document that you only want two people to access to. In this case you could make a `confidential document` custom permission and assign it to the document as well as the two users that you want to have access. The lack of the permission will block the user from being able to access the document.

## Create Custom Permission

{{< figure src="/images/user_permissions/user_permissions_3.png" caption="Create new custom permission view" width="1024">}}

When creating a custom permission we need to provide.

1. A permission name (in multiple languages if we support more than one).
2. The visibility of the permission in the system.
3. On what `department` the permission exists.

Finally we click the `Create New Permission` button to save the new custom permission.

