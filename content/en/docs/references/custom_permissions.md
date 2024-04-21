---
title: "Custom Permissions"
description: "In this section we look at the custom permissions and how they affect access to messages in the system."
lead: "In this section we look at the custom permissions and how they affect access to messages in the system."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "references"
weight: 100
toc: true
---

## Overview

Custom persmissions allows you to control access to different aspects of the systems. One example might to lock down message access to only users who have a specific role associated with them.

For example you want to create a Form that only allows users who have the `manage` custom role to access or use the form. In this case any messages created from this form will inherit the permission settings of the form meaning they will also only be accessible to users with the `manage` role.

## Global override permissions

There are some permissions that are global and will override custom permissions. These vary depending on the element that has custom roles associated with it. Below is a list of the global permissions that will always override custom permissions for different elements.

### Forms

| Role             | Id  | Description                                    |
| ---------------- | --- | ---------------------------------------------- |
| MENU_ADMIN_FORMS | `5` | The user has access to the Administrator Forms |

The permissions above will override any custom permissions set on a form as the user has access to all forms.

If we have a form that contains a custom role called Manager `any messages` created from this form will inherit this role when registered.

> This means that even if we remove this role from the form later it will not affect the existing messages that require this role as they are independent of the original role.
>
> This is done to ensure removing the role from the form does not immediately allow access to all the messages to everyone.

### Messages

| Role                         | Id   | Description                    |
| ---------------------------- | ---- | ------------------------------ |
| ACCESS_SEE_ALL_MESSAGES      | `57` | See all messages               |
| ACCESS_SEE_OTHER_USERS_CASES | `88` | User can see other users cases |

The permissions above will override any custom permissions set on a message as the user has acess to all messages.

> Note: `ACCESS_SEE_OTHER_USERS_CASES` is being planned to be removed in the future as it overlaps with `ACCESS_SEE_ALL_MESSAGES`.
