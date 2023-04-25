---
title: "Administrator/Tokens"
description: "En brukerveiledning for arbeid med tokens"
lead: "En brukerveiledning for arbeid med tokens. Vi dekker hvordan du oppretter og endrer tokens."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 25
toc: true
---
Denne delen handler om å håndtere tokens i systemet.

Klikk på `Administrator/Tokens` gir tilgang til listen over tokens.

## Tokenoversikt

{{< figure src="/images/tokens/tokens_3_no.png" caption="Oppføring av API-tokens" width="1024">}}

{{< figure src="/images/tokens/tokens_5_no.png" caption="Mobilbrukere pålogget oppføring" width="1024">}}

Det er to hovedtyper tokens i systemet.

| Token Type | Beskrivelse | 
| --- | --- |
| `API Tokens` | Tokens som brukes til å integrere med systemet ved hjelp av eksterne applikasjoner eller kode. |
| `Mobile Users Logged In` | Gir en oversikt over Mobile Application tokens, som lar deg se brukerne av mobilappen og tilbakekalle tilgang om nødvendig. |

> Tokens er knyttet til en `Bruker` og `Brukertype`. Dette lar deg kontrollere tilgang mer finmaskert ved å bruke tillatelser for å begrense tilgang. For eksempel kan du lage et token som bare tillater tilgang til avdeling A og ikke har tilgang til å operere på brukere.

## Slette Tokens

{{< figure src="/images/tokens/tokens_7_no.png" caption="Slette flere mobile brukertokens, tilbakekalle tilgang" width="1024">}}

Tokens kan også slettes for å tilbakekalle tilgang for både `API Tokens` og `Mobile Users Logged In`. Du kan slette dem enkeltvis eller bruke avkrysningsboksen på venstre side for å velge flere oppføringer å slette samtidig.

## Undersøke en Token

Å klikke på en Token viser informasjon om token. Denne skjermen er forskjellig avhengig av om det er en `API Token` eller `Mobile Users Logged In Token`.

{{< figure src="/images/tokens/tokens_6_no.png" caption="Mobile Users Logged In Token View" width="1024">}}

Når du velger en `Mobile User Token`, vises følgende informasjon.

| Felt | Beskrivelse |
| --- | --- |
| `Brukernavn` | Brukernavnet assosiert med token. |
| `E-post` | E-posten assosiert med token. |
| `Avdeling` | Avdelingen token er assosiert med. |
| `Brukertype` | Brukertypen token er assosiert med. |
| `Sist aktiv` | Siste gang brukeren var aktiv. |
| `Utløpsdato` | Gjeldende utløpsdato for token. |

{{< figure src="/images/tokens/tokens_2_no.png" caption="API-tokenvisning" width="1024">}}

`API Token`-visningen er litt forskjellig, fordi det forventes at du vil trenge tilgang til selve token.

| Felt | Beskrivelse |
| --- | --- |
| `Token Navn` | Navnet som ble angitt da du opprettet token. |
| `API Token` | Tokenstrengen som brukes til å ringe REST API. |
| `Tenant Id` | Applikasjonens kunde-ID. |
| `Bruksbeskrivelse` | Grunnleggende tekst som forklarer hvordan du bruker token for å kalle REST API-endepunktene. |
| `Utløpsdato` | Den angitte utløpsdatoen for denne API-token. |
| `Tilknyttet bruker` | Brukeren som brukes for å etablere tillatelser ved bruk av API-et. |
| `Avdeling og brukertype` | Kombinasjonen kontrollerer tilgang til data i systemet etter avdeling og brukertype. |

## Opprette en ny API-token

{{< figure src="/images/tokens/tokens_1_no.png" caption="Oprette ny token" width="1024">}}

Du kan opprette nye `API Tokens` for integrasjon. Følgende felt må fylles ut.

| Felt | Beskrivelse |
| --- | --- |
| `Token Navn` | Navnet som ble angitt da du opprettet token. |
| `Utløpsdato` | Angi utløpsdatoen for token, med en foreslått varighet på ikke lenger enn 12 måneder for en enkelt token. |
| `Velg bruker` | Velg brukeren som skal brukes for tillatelseskontroll. |
| `Velg avdeling og brukertype` | Velg `Avdeling` og `Brukertype` som er knyttet til denne token. |

Når du klikker på "Lagre," vil en ny API-token med en tilfeldig generert `token-streng` bli opprettet. Du kan deretter klikke på den token for å vise detaljene om token.

> For å garantere datasikkerhet, må du sørge for å gi token kun den minimale mengden tillatelser som er nødvendige for integrasjon.
