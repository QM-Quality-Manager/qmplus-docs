---
title: "Tilpassede Tillatelser"
description: "I denne delen ser vi på de tilpassede tillatelsene og hvordan de påvirker tilgangen til meldinger i systemet."
lead: "I denne delen ser vi på de tilpassede tillatelsene og hvordan de påvirker tilgangen til meldinger i systemet."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "referanser"
weight: 100
toc: true
---

## Oversikt

Tilpassede tillatelser lar deg kontrollere tilgangen til ulike deler av systemene. Et eksempel kan være å låse ned tilgangen til meldinger bare for brukere som har en spesifikk rolle tilknyttet dem.

For eksempel ønsker du å opprette et skjema som bare tillater brukere som har den tilpassede rollen `leder` tilgang til å bruke skjemaet. I dette tilfellet vil eventuelle meldinger som er opprettet fra dette skjemaet arve tillatelsesinnstillingene fra skjemaet, noe som betyr at de også bare vil være tilgjengelige for brukere med `leder`-rollen.

## Globale overstyringstillatelser

Det finnes noen tillatelser som er globale og vil overstyre tilpassede tillatelser. Disse varierer avhengig av elementet som har tilpassede roller tilknyttet seg. Nedenfor er en liste over de globale tillatelsene som alltid vil overstyre tilpassede tillatelser for ulike elementer.

### Skjemaer

| Rolle            | Id  | Beskrivelse                                      |
| ---------------- | --- | ------------------------------------------------ |
| MENU_ADMIN_FORMS | `5` | Brukeren har tilgang til administrasjonsskjemaer |

Tillatelsene ovenfor vil overstyre eventuelle tilpassede tillatelser satt på et skjema da brukeren har tilgang til alle skjemaer.

Hvis vi har et skjema som inneholder en tilpasset rolle kalt Manager, vil `alle meldinger` som er opprettet fra dette skjemaet arve denne rollen når de registreres.

> Dette betyr at selv om vi fjerner denne rollen fra skjemaet senere, vil det ikke påvirke de eksisterende meldingene som krever denne rollen, ettersom de er uavhengige av den opprinnelige rollen.
>
> Dette gjøres for å sikre at fjerning av rollen fra skjemaet ikke umiddelbart gir tilgang til alle meldingene til alle.

### Meldinger

| Rolle                        | Id   | Beskrivelse                        |
| ---------------------------- | ---- | ---------------------------------- |
| ACCESS_SEE_ALL_MESSAGES      | `57` | Se alle meldinger                  |
| ACCESS_SEE_OTHER_USERS_CASES | `88` | Bruker kan se andre brukeres saker |

Tillatelsene ovenfor vil overstyre eventuelle tilpassede tillatelser satt på en melding ettersom brukeren har tilgang til alle meldinger.

> Merk: `ACCESS_SEE_OTHER_USERS_CASES` planlegges fjernet i fremtiden da den overlapper med `ACCESS_SEE_ALL_MESSAGES`.
