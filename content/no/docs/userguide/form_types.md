---
title: "Administrator/Skjematyper"
description: "En brukerveiledning for arbeid med skjematyper"
lead: "En brukerveiledning for arbeid med skjematyper. Vi dekker hvordan du oppretter og endrer skjematyper."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 17
toc: true
---
Denne delen fokuserer på å håndtere skjematype innen systemet.

Ved å klikke på `Administrator/Skjematyper` får du tilgang til listen over skjematyper.

`Skjematyper` fungerer som en måte å gruppere `skjemaer` sammen på, slik at systemet kan bruke delte innstillinger på tvers av alle skjemaer basert på en bestemt skjematype.

## Liste over skjematyper

{{< zoomableImage src="/images/form_types/form_types_1_no.png" caption="Liste over skjematyper" width="1600" height="600px">}}

Du kan filtrere skjematyper etter status som `Aktiv` eller `Inaktiv` eller vise `Alle` sammen. Klikk på knappen til høyre for hver skjematype for å `Aktivere` eller `Deaktivere` en bestemt skjematype. I tillegg kan du opprette en ny `Skjematype` ved å klikke på `Opprett`-knappen.

### Opprette en ny skjematype

{{< zoomableImage src="/images/form_types/form_types_2_no.png" caption="Opprette en ny skjematype" width="1600" height="600px">}}

En skjematype lar deg håndtere et sett med forventninger for skjemaer basert på denne spesifikke `Skjematype`. For å opprette en, må du oppgi følgende alternativer:

| Felt | Beskrivelse |
| --- | --- |
| `Skjematype tittel` | Tittelen for skjematype, med støtte for flere språk. |
| `Arbeidsflyt` | Arbeidsflyten knyttet til alle skjemaer basert på denne `Skjematype`. |
| `Er det en risikoskjema` | Angir skjematype som en risikoskjema. |
| `Bakgrunnsfarge` | Angir bakgrunnsfargen for alle skjemaer basert på denne `Skjematype`. |
| `Beskrivelse` | En valgfri beskrivelse for en bestemt skjematype. |
| `Standard feltmal` | Gjør at du kan angi hvilke felter som skal inkluderes når du oppretter et nytt skjema basert på denne skjematype. |

De `Standard feltmal` typer inkluderer følgende:

| Felt | Beskrivelse |
| --- | --- |
| `Registrer på avdeling` | Felt som lar deg velge avdelingen der meldingen skal registreres. |
| `Hendelse inntruffet på` | Gir en komponent som lar deg angi dato/tidspunkt for når hendelsen knyttet til skjemaregistreringen skjedde. |
| `Velg saksbehandler` | Felt som lar deg velge saksbehandleren som skal motta skjemaoppføringen. |
| `Registrert av` | Et felt som lar brukeren som skriver inn en melding velge personen som registrerte meldingen. |
| `Registrert på vegne av` | Et felt som lar brukeren som skriver inn en melding velge personen de registrerer meldingen på vegne av. |
| `Beskrivelsesfelt` | Et felt som lar deg gi en beskrivelse som skal logges som en del av sakstittelen og informasjonen. |
| `Feilkostnad` | Et felt som lar deg angi en kostnad knyttet til registrering av en ny melding. |
| `Prioritetsfelt` | Et felt som lar deg velge prioriteten til meldingen som blir registrert. |