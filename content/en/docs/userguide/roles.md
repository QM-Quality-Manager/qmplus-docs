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
weight: 8
toc: true
---
This section addresses the management of user permissions within the system.

By clicking on `Administrator/User Permissions`, you can access the list of all available permissions.

There are two types of permissions in the system:

| Type | Description |
| --- | --- |
| `System` | System permissions control access to sections or actions within the application itself and are provided by the application. For example, these permissions might allow you to administer users or view reports. Users cannot customize these permissions, and they may expand as new functionalities are added. |
| `Custom` | Custom permissions are permissions that users can create to tag content, such as documents, or limit access to specific areas like departments. For instance, you might have a `confidential` document that only two people should have access to. In this case, you could create a `confidential document` custom permission and assign it to the document and the two users you want to grant access to. The absence of the permission will prevent users from accessing the document. |

[See all available System Permissions]({{< ref "/content/en/docs/references/permissions.md" >}} "System Permissions")

## Permissions List

### System Permissions

{{< figure src="/images/user_permissions/user_permissions_1.png" caption="System permissions list" width="1024">}}

The image above displays the list of `System Permissions`. You can filter these permissions to search for specific ones. `System Permissions` cannot be modified or deleted, and they represent all the `Application Level Permissions` available for your account. The number of available permissions may vary depending on your contract options.

A complete list of `System Permissions` can be found here.

### Custom Permissions

{{< figure src="/images/user_permissions/user_permissions_2.png" caption="Custom permissions list" width="1024">}}

Custom permissions are permissions that users can create to tag content, such as documents, or limit access to areas like departments. For instance, you might have a `confidential` document that only two people should have access to. In this case, you could create a `confidential document` custom permission and assign it to the document and the two users you want to grant access to. The absence of the permission will prevent users from accessing the document.

## Create Custom Permission

{{< figure src="/images/user_permissions/user_permissions_3.png" caption="Create new custom permission view" width="1024">}}

When creating a custom permission, you need to provide:

1. A permission name (in multiple languages if your system supports more than one language).
2. The visibility of the permission within the system.
3. The `department` in which the permission exists.

Finally, click the `Create New Permission` button to save the new custom permission.