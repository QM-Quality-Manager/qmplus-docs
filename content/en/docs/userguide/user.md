---
title: "Administrator/User"
description: "A user guide for working with users"
lead: "A user guide for working with users. We cover how to create and modify users."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 6
toc: true
---
This section deals with managing users in the system.

Clicking on the `Administrator/User` gives access to the list of users.

## User List
{{< figure src="/images/users/user_1.png" caption="User list overview" width="1024">}}

The user list shows you all the available users in the system. In this view we can choose between seeing the **Active**, **Inactive** and **All** users.

The search field lets you do a free text search to filter the users you currently see by first, middle or lastname as well as email and phone number.

Clicking the filter button lets you narrow the search even more as shown below.

{{< figure src="/images/users/user_13.png" caption="Filter users" width="1024">}}

The options for filtering are as following.

| Filter | Description |
| --- | --- |
| `Visibility` | Only show users in the `All departments`, `This department` or `Only child departments` |
| `User type` | Show only users who has the specific user type |
| `Permission/Role` | Show all users who have a specific permission/role |

All these filter can be combined to limit the search even more.

{{< figure src="/images/users/user_12.png" caption="New workflow dialog" width="1024">}}

## Create User

### General Settings

{{< figure src="/images/users/user_4.png" caption="New workflow dialog" width="1024">}}

The create user dialog lets us create new users for the system, and specify their usertypes as well as custom permissions. Finally we can adjust the notification settings.

The following are available.

| Field | Required | Description |
| --- | --- | --- |
| `Username` | **X** | The login username for the user (must be unique in the system) |
| `Password` | **X** | The users password |
| `Confirm password` | **X** | Confirm the password in this field |
| `First name` | **X** | The first name of the user |
| `Middle name` |  | The middle name of the user |
| `Last name` | **X** | The last name of the user |
| `Language` | **X** | The users preferred interface language |
| `Email` | **X** | The users email |
| `Phone` |  | The users phone number |
| `Comment` |  | Any commentary on the user, say additional information about the user created. |

Once these fields are filled in we have to assign at least one `department` and `user type` combination. Click on the `Types and Permissions` Tab.

### Avatar

We can modift the avatar for the user by clicking on the `avtar` circle. Options here are changing the background color, upload an image or capture an image with the web cam.

{{< figure src="/images/users/user_10.png" caption="Choose color of avatar or upload/webcam" width="1024">}}

Below we can see the dialog where we can upload an image or use the webcam (requires the user to give permissions to access the camera).

{{< figure src="/images/users/user_11.png" caption="Upload image or take webcam snap" width="1024">}}

Once you have uploaded an image or taking a photo with the webcam you can adjust the capture area and set the result.

{{< figure src="/images/users/user_15.png" caption="Adjust avatar image" width="1024">}}

### Department and User Types
{{< figure src="/images/users/user_5.png" caption="Department and user type view" width="1024">}}

Every user needs at least one `department` and `user type` combination added to it. A user can have multiple combinations of
`department` and `user type` but no duplicated roles.

> For example an administrator might have two combinations.
>
> For the top department they might be an `administrator`.
> At the same time they are an `employee` on another department.

{{< figure src="/images/users/user_7.png" caption="Select department" width="1024">}}

{{< figure src="/images/users/user_8.png" caption="Select user type" width="1024">}}

The effect of having multiple combinations of `department` and `user type` will lead to a dialog when logging in allowing you to pick which combination
you are going to log in as.

{{< figure src="/images/users/user_14.png" caption="Change department and usertype" width="1024">}}

You also get access to changing your department/user type combination in a pull down on the top right. Click on one of the combination will change your view
of the application allowing you to switch from for example an `employee` view of the organization to an `administrator` view.

### Custom Permissions/Roles

{{< figure src="/images/users/user_9.png" caption="Custom permissions/Roles" width="1024">}}

Besides setting combinations of `department` and `usertype` you can also add user specific permissions/roles. This lets you control the permissions of a specific user in a fine grained manner, using the user type as a starting point.

### Notifications

{{< figure src="/images/users/user_6.png" caption="Notification Tab" width="1024">}}

In the Notifications tab you can set the notification settings for the user.

## User Substitutions

### List View

{{< figure src="/images/users/user_2.png" caption="Substitutes list" width="1024">}}

The `User Substitutions` tab allows us to create `substitutions` for employees allwing us to delegate responsibility to other users for a specific amount of time.

> Substitutions can be used to delegate responsibilities in cases such as vacation, medical leave or parental leave.

As can se from the listing we get a complete list of the substitutions.

This lets us know the `person` being subsituted, who is substituting the person, what combination of `department` and `user type` the subsitution applies to and finally the duration of the subsitution.

> If we decide to delete a substitution entry, we have two scenarios.
> 
> 1. If the period is not active, the whole substituion is deleted
> 2. If we are already in the substitution period, it's cut short (end date is modified to the current date and time).

### Create Substitute

{{< figure src="/images/users/user_3.png" caption="New workflow dialog" width="1024">}}

We can create subsititutions of a user by another easily. First select the user to be substituted. This will then show you their list of `department` and `user type`. Pick which combination you wish to subsitute. Then select the `substituting` user and set the period the `substitution` is in effect. Finally click `Save` to create the subsitution rule.

> A `substituting` user will now see the additional `department` and `user type` combination show up in the list of available options when logging in.
>
> Data routed to the original user will now also be routed to the `subtitute` user instead of the original user.
