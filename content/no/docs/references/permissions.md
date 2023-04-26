---
title: "Programtillatelser"
description: "I denne delen gir vi en oversikt over tillatelsene (rollene) gitt på plattformen."
lead: "I denne delen gir vi en oversikt over tillatelsene (rollene) gitt på plattformen."
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
## Administrator meny tilgangsrettigheter
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| MENU_ADMIN | `14` | Brukeren har tilgang til Administrator Menyen |
| MENU_ADMIN_USERS | `1` | Brukeren har tilgang til Administrator Brukere |
| MENU_ADMIN_USER_TYPES | `3` | Brukeren har tilgang til Administrator Brukertyper |
| MENU_ADMIN_DEPARTMENTS | `2` | Brukeren har tilgang til Administrator Avdelinger |
| MENU_ADMIN_CATEGORIES | `4` | Brukeren har tilgang til Administrator Kategorier |
| MENU_ADMIN_FORMS | `5` | Brukeren har tilgang til Administrator Skjemaer |
| MENU_ADMIN_RULES | `6` | Brukeren har tilgang til Administrator Regler |
| MENU_ADMIN_DOCUMENTS | `7` | Brukeren har tilgang til Administrator Dokumenter |
| MENU_ADMIN_ROLES | `8` | Brukeren har tilgang til Administrator Roller |
| MENU_ADMIN_WORKFLOW | `86` | Brukeren har tilgang til Administrator Arbeidsflyt |
| MENU_ADMIN_LISTS | `90` | Brukeren har tilgang til Administrator Lister |
| MENU_ADMIN_RISK_MODEL | `170` | Brukeren har tilgang til Administrator Risikomodeller |
| MENU_ADMIN_USER_ACCESS | `171` | Brukeren har tilgang til Administrator API Tokens |
| MENU_ADMIN_ACTIVITIES | `66` | Brukeren har tilgang til Administrator Aktiviteter |
| MENU_ADMIN_REPORTS | `91` | Brukeren har tilgang til Administrator Rapporter |
| MENU_ADMIN_TASK_TEMPLATE_MENU | `92` | Brukeren har tilgang til Oppgavemaler |

## Tilgang systemadministrator rettigheter
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| ACCESS_SYSTEM_ADMINISTRATOR | `9` | Brukeren kan opprette/oppdatere/slette brukertyper og tilordne brukertyper og roller til brukere. |

> `MENU_ADMIN_USERS` gir deg tilgang til å oppdatere alle brukerinnstillinger bortsett fra brukertypeinnstillinger. For å oppdatere bruker brukertyper og roller trenger du også `ACCESS_SYSTEM_ADMINISTRATOR`-rollen. Dette er for å sikre at bare utvalgte personer kan endre tilgangsnivåene til en gitt bruker.

## Funksjonalitet tilgjengelig for brukeren
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| MENU_DOCUMENTS | `12` | Brukeren har tilgang til Dokumentvisningen |
| MENU_ACTIVITYPLAN | `15` | Brukeren har tilgang til Aktivitetsplanvisningen |
| MENU_CASES | `29` | Brukeren har tilgang til Saksbordvisningen |
| MENU_NAVIGATOR | `64` | Brukeren har tilgang til Avdelingsnavigator |
| MENU_GRAPHS_USER_REPORTS | `70` | Brukeren har tilgang til Rapporter |
| MENU_HOME | `80` | Brukeren har tilgang til Hjem (kan logge inn) |
| MENU_SEARCH | `83` | Brukeren kan søke (ser søkefelt) |
| MENU_CASE_BOARD | `110` | Brukeren kan få tilgang til Saksbordet |
| MENU_DASHBOARD | `123` | Brukeren kan få tilgang til Dashbordene |
| MENU_PUBLISHER | `130` | Brukeren kan få tilgang til Utgivermenyen |
| MENU_MARKETPLACE | `140` | Brukeren kan få tilgang til Markedsplassen |
| MENU_INTEGRATIONS | `150` | Brukeren kan få tilgang til Integrasjonsmenyene |
| MENU_BILLING | `180` | Brukeren kan få tilgang til Faktureringsmenyene |
| MENU_QUESTIONNAIRES | `190` | Brukeren kan få tilgang til Spørreskjema Menyen |
| MENU_SETTINGS | `33` | Brukeren kan få tilgang til Preferansemenyene |
| MENU_CASE_MESSAGES | `230` | Brukeren kan få tilgang til Meldingssaker |
| MENU_CASE_ACTION | `231` | Brukeren kan få tilgang til Aksjonssaker |
| MENU_CASE_HEARING | `232` | Brukeren kan få tilgang til Høringssaker |
| MENU_CASE_AUDIT | `233` | Brukeren kan få tilgang til Revisjonssaker |
| MENU_CASE_DOCUMENT | `234` | Brukeren kan få tilgang til Dokumentsaker |

## Endringsrettigheter
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| ACCESS_CONTENT_ADMINISTRATOR | `19` | Innholdsadministrator |
| ACCESS_MOVE_MESSAGE | `81` | Brukeren kan flytte meldinger mellom avdelinger |
| ACCESS_SEE_OTHER_USERS_CASES | `88` | Brukeren kan se andre brukeres saker |
| ACCESS_PROCESS_MESSAGE | `55` | Behandle melding |
| ACCESS_PROCESS_ACTION | `160` | Tilgang til å behandle aksjon |
| ACCESS_PROCESS_DOCUMENT | `163` | Behandle dokument |
| ACCESS_PROCESS_HEARING | `164` | Behandle høring |
| ACCESS_PROCESS_AUDIT | `165` | Behandle revisjon |
| ACCESS_CREATE_MESSAGE | `53` | Opprette / Redigere melding |
| ACCESS_SEE_ALL_MESSAGES | `57` | Se alle meldinger |

## Sakshåndtering/varsel
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| BEHAVIOUR_DEFAULT_MESSAGE_RECEIVER | `50` | Standard mottaker av meldinger |
| BEHAVIOUR_DEFAULT_POSSIBLE_MESSAGE_RECEIVER | `51` | Standard mulig meldingsmottaker |
| BEHAVIOUR_DEFAULT_POSSIBLE_INFORMATION_RECEIVER | `52` | Standard mulig informasjonsmottaker |

## Dashboardrettigheter
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| DASHBOARD_CREATE_PERMISSION | `120` | Opprette dashbord |
| DASHBOARD_UPDATE_PERMISSION | `121` | Oppdatere dashbord |
| DASHBOARD_DELETE_PERMISSION | `122` | Slette dashbord |
| DASHBOARD_ADD_GENERAL_COMPONENT | `124` | Opprette generelle dashboardkomponenter |

## Utgiverrettigheter (for Markedsplass)
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| PUBLISHER_UPDATE_PERMISSION | `131` | Oppdatere utgiver |
| PUBLISHER_CREATE_PACKAGE_PERMISSION | `132` | Opprette utgiverpakke |
| PUBLISHER_UPDATE_PACKAGE_PERMISSION | `133` | Oppdatere utgiverpakke |
| PUBLISHER_PUBLISH_PERMISSION | `134` | Publiseringsrettighet |

> Bare tilgjengelig hvis du har kontrakt for Markedsplass-støtte

## Markedsplass-rettigheter
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| MARKETPLACE_PURCHASE | `141` | Kjøp på markedsplassen |
| MARKETPLACE_IMPORT | `142` | Import fra markedsplassen |

> Bare tilgjengelig hvis du har kontrakt for Markedsplass-støtte

## Rettighet til å oppdatere integrasjonsinnstillinger
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| INTEGRATIONS_UPDATE | `151` | Oppdatering av integrasjon |

> Bare tilgjengelig hvis du har kontrakt for Integreringsstøtte

## Rettigheter for sakshåndtering
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| DELETE_PROCESS_CASE | `161` | Slette sak |
| CLOSE_PROCESS_MESSAGE | `162` | Lukke melding |

## Faktureringsrettigheter
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| BILLING_NOTIFICATIONS | `181` | Faktureringsvarsler |

> Bare tilgjengelig hvis du har registrert deg via kredittkort

## Kontaktrettighet
| Rolle | Id | Beskrivelse |
| ------- | ------- | ------- |
| SYSTEM_ADMINISTRATOR_CONTACT | `200` | Brukeren er en systemadministrator-kontakt (superbruker), brukt til å merke en bruker som en kontaktperson for organisasjonen som en mulig ressurs for plattformen. |