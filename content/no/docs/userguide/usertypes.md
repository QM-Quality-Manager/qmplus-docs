---
title: "Administrator/Brukertyper"
description: "En brukerveiledning for arbeid med brukertyper"
lead: "En brukerveiledning for arbeid med brukertyper. Vi dekker hvordan du oppretter og endrer brukertyper."
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
En brukertype er en samling av roller som representerer spesifikke grupperinger av tillatelser med et tilordnet navn. Eksempler på brukertyper kan være **Administrator**, **Ansatt** og **Inspektør**, der hver brukertype inneholder et sett med roller som gir brukeren tillatelser til å utføre forskjellige handlinger eller få tilgang til bestemte funksjoner på plattformen.

## Hovedadministrator-skjerm
{{< zoomableImage src="/images/usertypes/usertype_1.png" caption="Hovedadministrator-skjerm" width="1600" height="600px">}}

Ved å klikke på `Administrator/Brukertyper` får du tilgang til listen over brukertyper.

Fra denne skjermen kan du utføre følgende handlinger:

### Velg brukertyper
Bytt mellom å vise alle brukertyper, gjeldende aktive brukertyper og inaktive brukertyper.

### Filtrer brukertyper
Bruk søkeboksen til å filtrere brukertyper ved å skrive inn relevant tekst.

### Aktiver/Deaktiver
Klikk på symbolet for å deaktivere en aktiv brukertype eller aktivere en inaktiv brukertype. Deaktivering av en brukertype sikrer at den ikke kan tilordnes andre brukere.

### Opprett en brukertype
Klikk på `Opprett`-knappen for å åpne dialogboksen "opprett ny brukertype".

## Opprett en ny brukertype
Dialogboksen "opprett ny brukertype" lar deg opprette en ny samling av tillatelser med et tilordnet navn.

{{< zoomableImage src="/images/usertypes/usertype_2.png" caption="Opprett ny brukertype-dialog" width="1600" height="600px">}}

En ny brukertype krever følgende felt, som vist på bildet:

| Felt | Beskrivelse |
| --- | --- |
| `Navn` | Navnet på brukertypen; hvis flere språk er konfigurert for kontoen din, kan du skrive inn navnet på flere språk. |
| `Beskrivelse` | Beskrivelsen av brukertypen; hvis flere språk er konfigurert for kontoen din, kan du skrive inn beskrivelsen på flere språk. |
| `Avdeling` | Avdelingen som denne brukertypen er konfigurert for. Kan brukes til å begrense tilgjengeligheten av brukertyper til bestemte avdelinger. |
| `Tillatelser` | Listen over alle tillatelser som er tilordnet denne spesifikke brukertypen. |

Etter å ha fylt ut feltene `Navn` og `Beskrivelse`, velg avdeling (eller la den stå på gjeldende avdeling) og klikk deretter på `Konfigurer tillatelser`-koblingen for å åpne sidefeltet.

> En liste over alle `System`-nivå tillatelser og deres betydning.
>
> [Oversikt over alle tillatelser]({{< ref "/docs/references/permissions" >}} "Oversikt over alle tillatelser")

{{< zoomableImage src="/images/usertypes/usertype_3.png" caption="Konfigurer tillatelser-sidefelt" width="1600" height="600px">}}

Her kan du velge `System`- og `Egendefinerte` roller som du ønsker å legge til i brukertypen du oppretter.

{{< zoomableImage src="/images/usertypes/usertype_4.png" caption="Velg roller" width="1600" height="600px">}}

Etter at du har valgt ønskede roller, klikk på knappen for å angi tillatelsene på brukertypen.

{{< zoomableImage src="/images/usertypes/usertype_5.png" caption="Angi tillatelser" width="1600" height="600px">}}

Til slutt, klikk på `Lagre`-knappen for å opprette brukertypen.