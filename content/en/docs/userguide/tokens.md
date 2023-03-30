---
title: "Administrator/Tokens"
description: "A user guide for working with tokens"
lead: "A user guide for working with tokens. We cover how to create and modify tokens."
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
This section deals with managing tokens in the system.

Clicking on the `Administrator/Tokens` gives access to the list of tokens.

## Tokens Listing

{{< figure src="/images/tokens/tokens_3.png" caption="API Tokens Listing" width="1024">}}

{{< figure src="/images/tokens/tokens_5.png" caption="Mobile users logged in Listing" width="1024">}}

There are two main types of tokens in the system.

| Token Type | Description | 
| --- | --- |
| `API Tokens` | Tokens used to integrate with Q using external applications or code. |
| `Mobile users logged in` | An overview of Mobile Application tokens, allowing us to view who uses the Mobile App and also revoke access. |

> Tokens are tied to a `User` and `User Type`. This allows you to control access more fine-grained by using permissions to restrict acces. You might for example make a token that only allows access to Department A and has no access to operate on users.

## Deleting Tokens

{{< figure src="/images/tokens/tokens_7.png" caption="Deleting multiple mobile user tokens, revoking access" width="1024">}}

Tokens can also be deleted to revoke access both for the `API Token` and `Mobile Users logged in`. Either one by one or by using the checkbox on the left side to select multiple entries to delete at the same time.

## Inspect a Token

Clickin on a Token will bring up information about the token. This screen is different depending on if it's an `API Token` or `Mobile users logged in Token`.

{{< figure src="/images/tokens/tokens_6.png" caption="Mobile Users logged in token view" width="1024">}}

When selecting a `Mobile User Token` you get the following information.

| Field | Description |
| --- | --- |
| `User name` | The user name associated with the token. |
| `Email` | The email associated with the token. |
| `Department` | The department the token is associated with. |
| `User Type` | The user type the token is associated with. |
| `Last active` | Last time the user was active. |
| `Expiry date` | The current expiry date for the token. |

{{< figure src="/images/tokens/tokens_2.png" caption="API Token view" width="1024">}}

The `API Token` view is a litte bit different because our expectation is that you will need access to the actual token.

| Field | Description |
| --- | --- |
| `Token name` | The name entered when creating the token. |
| `API Token` | The token string used to call the REST API. |
| `Tenant Id` | Application customer Id. |
| `Description of use` | Basic text that explains how to use the token to call the REST API endpoints. |
| `Expiry date` | The entered expiry date for this API token. |
| `Associated user` | The user used to establish permissions when using the API. |
| `Department and User Type` | The combination controls access to data in the system by Department and User Type. |

## Create a new API Token

{{< figure src="/images/tokens/tokens_1.png" caption="" width="1024">}}

We can create new `API Token` to use for integration. We need to provide the following fields.

| Field | Description |
| --- | --- |
| `Token name` | The name entered when creating the token. |
| `Expiry date` | Set the expiry date of the token, we suggest no longer than 12 months for any single token. |
| `Select user` | Select the user who will be used for permissions checking. |
| `Select department & user type` | Select the `Department` and `User Type` associated with this token. |

When we click save a new API token with a random new `token string` will be created. You can click on that token to view the details of the token.

> Ensure you only give the token the minimum amount of permissions needed to integrate to ensure data safety.
