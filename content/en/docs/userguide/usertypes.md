---
title: "Administrator/User Types"
description: "A user guide for working with user types"
lead: "A user guide for working with user types. We cover how to create and modify user types."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 7
toc: true
---
A user type is a collection of roles that represents specific groupings of permissions with an assigned name. Examples of user types can include **Administrator**, **Employee**, and **Inspector**, where each user type contains a set of roles that grant the user permissions to perform different actions or access specific features of the platform.

## Main Administrator Screen
{{< figure src="/images/usertypes/usertype_1.png" caption="Main administrator screen" width="1024">}}

Clicking on the `Administrator/User Types` gives you access to the list of user types.

From this screen, you can perform the following actions:

### Select User Types
Switch between viewing all user types, currently active user types, and inactive user types.

### Filter User Types
Use the search box to filter user types by entering relevant text.

### Activate/Deactivate
Click on the symbol to deactivate an active user type or activate an inactive user type. Deactivating a user type ensures that it cannot be assigned to other users.

### Create a User Type
Click the `Create` button to open the "create new user type" dialog.

## Create a New User Type
The "create new user type" dialog allows you to create a new collection of permissions with an assigned name.

{{< figure src="/images/usertypes/usertype_2.png" caption="Create new user type dialog" width="1024">}}

A new user type requires the following fields, as shown in the image:

| Field | Description |
| --- | --- |
| `Name` | The name of the user type; if multiple languages are configured for your account, you can enter the name in multiple languages. |
| `Description` | The description of the user type; if multiple languages are configured for your account, you can enter the description in multiple languages. |
| `Department` | The department for which this user type is configured. Can be used to limit the availability of user types to specific departments only. |
| `Permissions` | The list of all permissions assigned to this specific user type. |

After filling out the `Name` and `Description` fields, select the department (or leave it on the current department), and then click the `Configure permissions` link to open the sidebar.

> A list of all `System` level permissions and their meanings.
>
> [Overview of all Permissions]({{< ref "/docs/references/permissions" >}} "Overview of all Permissions")

{{< figure src="/images/usertypes/usertype_3.png" caption="Configure permissions sidebar" width="1024">}}

Here, you can select `System` and `Custom` roles that you want to add to the user type you are creating.

{{< figure src="/images/usertypes/usertype_4.png" caption="Select roles" width="1024">}}

After selecting the desired roles, click the button to set the permissions on the user type.

{{< figure src="/images/usertypes/usertype_5.png" caption="Set permissions" width="1024">}}

Finally, click the `Save` button to create the user type.