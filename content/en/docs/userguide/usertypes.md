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
A user type is a collection of roles. It is used to create specific grouping of permissions and give them a name. Examples of user types can be **Administrator**, **Employee**, **Inspector** where each usertypes contains a set of roles that gives the user permissions to perform different actions or have access to specific features of the platform.

## Main Administrator Screen
{{< figure src="/images/usertypes/usertype_1.png" caption="New workflow dialog" width="1024">}}

Clicking on the `Administrator/User Types` gives access to the list of user types.

You can take the following actions from this screen.

### Select User types
You can switch beetween viewing all the user types, the currently active user types and the inactive user types.

### Filter User types
The search box lets us filter down the usertypes by entering free text.

### Activate/Deactivate
Clicking on the symbol lets you deactivate an active user type or activate an inactive user type.

Inactivating a user type lets you ensure it's not possible to assign it to other users.

### Create a user type
Clicking the `Create` button will bring up a create new user type dialog.

## Create a New User Type
The create new user type dialog lets you create a new collection of permissions and give it a name.

{{< figure src="/images/usertypes/usertype_2.png" caption="New workflow dialog" width="1024">}}

A new user type requires the following fields as shown in the image.

| Field | Description |
| --- | --- |
| `Name` | The name of the user type, if multiple languages are configured for your account you'll be able to enter the name in multiple languages. |
| `Description` | The description of the user type, if multiple languages are configured for your account you'll be able to enter the description in multiple languages. |
| `Department` | The department this user type is configured on. Can be used to limit the ability of user types to specific departments only.|
| `Permissions` | The list of all the permissions assigned to this specific user type. |

After having filled out the `Name` and `Description` field, select the department (or leave it on the current department) and then finally click the `Configure permissions` link to bring up the sidebar. 

> A list of all `System` level permissions and their meaning.
>
> [Overview of all Permissions]({{< ref "/docs/references/permissions" >}} "Overview of all Permissions")

{{< figure src="/images/usertypes/usertype_3.png" caption="New workflow dialog" width="1024">}}

Here you can select `System` and `Custom` roles that you want to add to the user type you are creating.

{{< figure src="/images/usertypes/usertype_4.png" caption="New workflow dialog" width="1024">}}

After selecting two roles we can then click the button to set the permissions on the user type.

{{< figure src="/images/usertypes/usertype_5.png" caption="New workflow dialog" width="1024">}}

Finally click the `Save` button to create the user type.
