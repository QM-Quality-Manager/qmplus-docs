---
title: "Administrator/Oppgavemaler"
description: "En brukerveiledning for arbeid med oppgavemaler"
lead: "En brukerveiledning for arbeid med oppgavemaler. Vi dekker hvordan man oppretter og endrer oppgavemaler."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 15
toc: true
---
Denne delen omhandler administrasjon av oppgavemaler i systemet.

Ved å klikke på `Administrator/Oppgavemaler`, får du tilgang til listen over oppgavemaler.

`Oppgavemaler` lar deg opprette lister over oppgaver som vil bli lagt til i nye `Saker` når en `Melding` blir registrert. For eksempel kan du opprette en liste over oppgaver som skal utføres hver gang en ulykkesmelding blir logget i systemet.

Du kan også legge til ytterligere oppgaver hvis spesifikke kategorier blir valgt av brukeren mens de fyller ut skjemaet. Dette lar deg lage dynamiske oppgavemaler som kan legge til supplerende oppgaver avhengig av selve skjemainngangen.

> Oppgavemaler fungerer som et kraftig middel for å standardisere oppgavesjekklister i organisasjonen for gitte `Skjema`-innganger.

## Liste over oppgavemaler

{{< zoomableImage src="/images/tasks_templates/tasks_templates_2_no.png" caption="Liste over oppgavemaler" width="1600" height="600px">}}

`Oppgavemaler`-listen viser alle de nåværende `Oppgavemalene` som er tilgjengelige for visning.

> Listen vil endre seg når du bytter avdelinger i organisasjonen, siden `Oppgavemaler` kan registreres for en bestemt avdeling og tildeles en organisatorisk synlighetstype (synlig innenfor avdelingen, synlig innenfor avdelingen og dens underavdelinger osv.).

## Opprett en ny oppgavemal

{{< zoomableImage src="/images/tasks_templates/tasks_templates_3_no.png" caption="Opprett en ny oppgavemal" width="1600" height="600px">}}

Når du oppretter en ny oppgavemal, har du følgende alternativer:

| Alternativ | Beskrivelse |
| --- | --- |
| `Oppgavemalens navn` | Angi navnet for å identifisere `Oppgaver`-malen, støtter flere språk. |
| `Beskrivelse` | Angi beskrivelsen for `Oppgaver`-malen. |
| `Synlighet` | Angi organisatorisk synlighet (avdeling, avdeling og underavdelinger). |
| `Avdeling` | Avdelingen der `Oppgaver`-malen er registrert. |
| `Legg til oppgave` | Legg til en `Mal`-oppgave i `Oppgaver`-malen. |

Klikk på `Lagre`-knappen for å lagre gjeldende status for `Oppgavemalen`.

### Legge til en ny oppgave

{{< zoomableImage src="/images/tasks_templates/tasks_templates_4_no.png" caption="Legge til en ny oppgavemal" width="1600" height="600px">}}

Når du klikker på `Legg til oppgave`-knappen, åpnes sidefeltet med alternativer for en ny oppgave. Følgende alternativer er tilgjengelige:

| Alternativ | Beskrivelse |
| --- | --- |
| `Navn` | Navnet på oppgaven som skal legges til i `Oppgaver`-malene. |
| `Kategorier` | Liste over kategorier som vil utløse tillegg av denne spesifikke oppgaven til en ny `Sak` når en skjemamelding er registrert. |

Klikk på `Konfigurer`-knappen for å hente listen over tilgjengelige kategorier. Til slutt, klikk på `Lagre endringer`-knappen for å lagre `Oppgaven` i `Oppgavemalen`.

### Velg kategorier

{{< zoomableImage src="/images/tasks_templates/tasks_templates_5_no.png" caption="Velg kategorier" width="1600" height="600px">}}

Etter at du har klikket på `Konfigurer`-knappen, kan du søke og velge kategoriene som vil utløse tillegg av `Oppgaven` som opprettes.

## Redigere en oppgavemal

{{< zoomableImage src="/images/tasks_templates/tasks_templates_6_no.png" caption="Redigere en oppgavemal" width="1600" height="600px">}}

Når du redigerer en `Oppgavemal`, kan du dra individuelle oppgaver opp og ned for å omorganisere dem i henhold til ønsket rekkefølge når de legges til i en `Sak`.

> Vi anbefaler å ikke starte navn med et tall hvis man bruker `kategorier`-filteret, da det kan føre til at lister mangler kontinuitet. For eksempel, hvis du legger til oppgavene 1. A, 2. B, 3. C og oppgave 2 er avhengig av en kategori, kan du ende opp med en `Sak`-oppgaveliste som inneholder bare 1. A og 3. C, noe som kan forvirre brukere.

Du kan også `Redigere`, `Vise` og `Slette` individuelle oppgaver i `Oppgavemalen`.

## Koble oppgavemal til skjema

{{< zoomableImage src="/images/tasks_templates/tasks_templates_8_no.png" caption="Koble oppgavemal til skjema" width="1600" height="600px">}}

Når du oppretter eller redigerer et `Skjema`, har du muligheten til å knytte en `Oppgavemal` fra listen over maler som er synlige for brukerens nåværende avdeling.

{{< zoomableImage src="/images/tasks_templates/tasks_templates_9_no.png" caption="" width="1600" height="600px">}}

Når en bruker registrerer en ny melding ved hjelp av dette skjemaet, vil den resulterende `Saken` inkludere en liste over `Oppgaver` basert på den tilknyttede `Oppgavemalen`. Dette sikrer at passende oppgaver genereres for hver sak i henhold til de forhåndsdefinerte malene, og bidrar til å opprettholde konsistens og overholdelse av organisatoriske prosesser.
