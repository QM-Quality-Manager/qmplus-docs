---
title: "Application Permissions"
description: "In this section we provide an overview of the permissions (roles) provided on the platform."
lead: "In this section we provide an overview of the permissions (roles) provided on the platform."
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
## Administrator menu access permissions
| Role | Id | Description |
| ------- | ------- | ------- |
| MENU_ADMIN | `14` | The user had access to the Administrator Menu |
| MENU_ADMIN_USERS | `1` | The user had access to the Administrator User |
| MENU_ADMIN_USER_TYPES | `3` | The user has access to the Administrator Usertypes |
| MENU_ADMIN_DEPARTMENTS | `2` | The user has access to the Administrator Departments |
| MENU_ADMIN_CATEGORIES | `4` | The user has access to the Administrator Categories |
| MENU_ADMIN_FORMS | `5` | The user has access to the Administrator Forms |
| MENU_ADMIN_RULES | `6` | The user has access to the Administrator Rules |
| MENU_ADMIN_DOCUMENTS | `7` | The user has access to the Administrator Documents |
| MENU_ADMIN_ROLES | `8` | The user has access to the Administrator Roles |
| MENU_ADMIN_WORKFLOW | `86` | The user has access to the Administrator Workflows |
| MENU_ADMIN_LISTS | `90` | The user has access to the Administrator Lists |
| MENU_ADMIN_RISK_MODEL | `170` | The user has access to the Administrator Risk Models |
| MENU_ADMIN_USER_ACCESS | `171` | The user has access to the Administrator API Tokens |
| MENU_ADMIN_ACTIVITIES | `66` | The user has access to the Administrator Activities |
| MENU_ADMIN_REPORTS | `91` | The user has access to the Administrator Reports |
| MENU_ADMIN_TASK_TEMPLATE_MENU | `92` | The user has access to the Tasks Templates |

## Access system administrator permissions
| Role | Id | Description |
| ------- | ------- | ------- |
| ACCESS_SYSTEM_ADMINISTRATOR | `9` | The user can create/update/delete user types as well as assign usertypes and roles to users. |

> `MENU_ADMIN_USERS` gives you access to update all user settings except the user type settings. To update user usertypes and roles you need the `ACCESS_SYSTEM_ADMINISTRATOR` role aswell. This is to ensure that only select people can change the access levels of a given user.

## Functionality available to the user
| Role | Id | Description |
| ------- | ------- | ------- |
| MENU_DOCUMENTS | `12` | The user has access to the Documents View |
| MENU_ACTIVITYPLAN | `15` | The user has access to the Activities Plan View |
| MENU_CASES | `29` | The user has access to the Caseboard View |
| MENU_NAVIGATOR | `64` | The user has access to the Department Navigator |
| MENU_GRAPHS_USER_REPORTS | `70` | The user has access to the Reports |
| MENU_HOME | `80` | The user has access to the Home (can login) |
| MENU_SEARCH | `83` | The user can search (sees search bar) |
| MENU_CASE_BOARD | `110` | The user can access the Caseboard |
| MENU_DASHBOARD | `123` | The user can access the Dashboards |
| MENU_PUBLISHER | `130` | The user can access the Publisher Menu |
| MENU_MARKETPLACE | `140` | The user can access the Marketplace |
| MENU_INTEGRATIONS | `150` | The user can access the Integrations Menus |
| MENU_BILLING | `180` | The user can access the Billing Menus |
| MENU_QUESTIONNAIRES | `190` | The user can access the Questionnaires Menu |
| MENU_SETTINGS | `33` | The user can access the Preferences Menus |
| MENU_CASE_MESSAGES | `230` | The user can access the Message Cases |
| MENU_CASE_ACTION | `231` | The user can access the Action Cases |
| MENU_CASE_HEARING | `232` | The user can access the Hearing Cases |
| MENU_CASE_AUDIT | `233` | The user can access the Audit Cases |
| MENU_CASE_DOCUMENT | `234` | The user can access the Document Cases |

## Modification permissions
| Role | Id | Description |
| ------- | ------- | ------- |
| ACCESS_CONTENT_ADMINISTRATOR | `19` | Content administrator |
| ACCESS_MOVE_MESSAGE | `81` | User can move messages between departments |
| ACCESS_SEE_OTHER_USERS_CASES | `88` | User can see other users cases |
| ACCESS_PROCESS_MESSAGE | `55` | Process message |
| ACCESS_PROCESS_ACTION | `160` | Acess process action |
| ACCESS_PROCESS_DOCUMENT | `163` | Process document |
| ACCESS_PROCESS_HEARING | `164` | Process hearing |
| ACCESS_PROCESS_AUDIT | `165` | Process audit |
| ACCESS_CREATE_MESSAGE | `53` | Create / Edit message |
| ACCESS_SEE_ALL_MESSAGES | `57` | See all messages |

## Case handling/notification
| Role | Id | Description |
| ------- | ------- | ------- |
| BEHAVIOUR_DEFAULT_MESSAGE_RECEIVER | `50` | Default message receiver |
| BEHAVIOUR_DEFAULT_POSSIBLE_MESSAGE_RECEIVER | `51` | Default possible message receiver |
| BEHAVIOUR_DEFAULT_POSSIBLE_INFORMATION_RECEIVER | `52` | Default possible information receiver |

## Dashboard permissions
| Role | Id | Description |
| ------- | ------- | ------- |
| DASHBOARD_CREATE_PERMISSION | `120` | Create Dashboards |
| DASHBOARD_UPDATE_PERMISSION | `121` | Update Dashboards |
| DASHBOARD_DELETE_PERMISSION | `122` | Delete Dashboards |
| DASHBOARD_ADD_GENERAL_COMPONENT | `124` | Create dashboard general components |

## Publisher permissions (for Marketplace)
| Role | Id | Description |
| ------- | ------- | ------- |
| PUBLISHER_UPDATE_PERMISSION | `131` | Update publisher |
| PUBLISHER_CREATE_PACKAGE_PERMISSION | `132` | Create publisher package |
| PUBLISHER_UPDATE_PACKAGE_PERMISSION | `133` | Update publisher package |
| PUBLISHER_PUBLISH_PERMISSION | `134` | Publish right |

> Only available if you have Marketplace support contracted

## Marketplace permissions
| Role | Id | Description |
| ------- | ------- | ------- |
| MARKETPLACE_PURCHASE | `141` | Marketplace purchase |
| MARKETPLACE_IMPORT | `142` | Marketplace import |

> Only available if you have Marketplace support contracted

## Permission to allow updating integration settings
| Role | Id | Description |
| ------- | ------- | ------- |
| INTEGRATIONS_UPDATE | `151` | Integration update |

> Only available if you have Integrations support contracted

## Cases process permissions
| Role | Id | Description |
| ------- | ------- | ------- |
| DELETE_PROCESS_CASE | `161` | Delete case |
| CLOSE_PROCESS_MESSAGE | `162` | Close message |

## Billing permissions
| Role | Id | Description |
| ------- | ------- | ------- |
| BILLING_NOTIFICATIONS | `181` | Billing notifications |

> Only available if you have signuped via credit card

## Contact permission
| Role | Id | Description |
| ------- | ------- | ------- |
| SYSTEM_ADMINISTRATOR_CONTACT | `200` | User user is a system administrator contact (super user), used to mark a user as a contact person for the organization as a possible resource for the platform. |
