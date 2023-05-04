---
title: "Administrator/Risikomodeler"
description: "En brukerveiledning for arbeid med risikomodeller"
lead: "En brukerveiledning for arbeid med risikomodeller. Vi dekker hvordan du oppretter og modifiserer risikomodeller."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 12
toc: true
---
Denne delen omhandler håndtering av risikomodeller i systemet.

Ved å klikke på `Administrator/Risikomodeler` får du tilgang til listen over risikomodeller.

## Liste over risikomodeller

{{< zoomableImage src="/images/risk_models/risk_model_1_no.png" caption="Liste over risikomodeller" width="1600" height="600px">}}

Listen over risikomodeller kan filtreres etter `aktive/deaktiverte eller alle`. Du kan også `aktivere / deaktivere` risikomodeller, noe som gjør dem usynlige når du oppretter nye kategorigrupper.
Til slutt vil du ved å klikke på `Opprett`-knappen kunne opprette en ny `Risikomodell`.

## Opprett ny risikomodell

### Generelle sider

{{< zoomableImage src="/images/risk_models/risk_model_2_no.png" caption="Generell side" width="1600" height="600px">}}

For å opprette en ny `Risikomodell` må vi angi et navn for risikomodellen (den støtter flere språk). Man kan også legge til en valgfri beskrivelse for modellen.

### Bygging av risikomodell

{{< zoomableImage src="/images/risk_models/risk_model_3_no.png" caption="Bygging av en risikomodell" width="1600" height="600px">}}

En risikomodell består av dimensjoner som inneholder skalaer med verdier som brukes til å beregne en endelig poengsum.

> For eksempel kan du ha en `Sannsynlighet`-skala samt en `Påvirkning`-skala, der hver skala i hver dimensjon har en tilknyttet verdi.

Når man legger inn en risikoverdi, vil brukeren velge en verdi fra hver dimensjon, og plattformen vil deretter beregne en tilsvarende risikoverdi avhengig av formelen knyttet til risikomodellen.

Når du legger til skalaer i dimensjonene, kan du se forhåndsvisningen av risikomodellen til venstre. For å definere farger basert på beregnede verdier i risikomatrisen, kan vi oppgi områder med tilknyttede farger ved å legge til og endre fargeområdenivåene nederst til høyre.

{{< zoomableImage src="/images/risk_models/risk_model_4_no.png" caption="Grunnleggende risikomodell-eksempel" width="1600" height="600px">}}

Denne modellen viser en fullstendig grunnleggende risikomodell med tilhørende dimensjoner, skalaer og fargeområder.

{{< zoomableImage src="/images/risk_models/risk_model_6_no.png" caption="Legge til en ny skala eller dimensjon" width="1600" height="600px">}}

Når du legger til eller redigerer en ny `skala` for en `dimensjon`, kan vi oppgi et navn, en beskrivelse og en verdi for skalaen.

### Versjonering av risikomodell

{{< zoomableImage src="/images/risk_models/risk_model_5_no.png" caption="Risikomodellversjoner" width="1600" height="600px">}}

Alle risikomodeller er versjonert. Dette gjøres slik at endringer i en risikomodell ikke påvirker eksisterende skjemaer.