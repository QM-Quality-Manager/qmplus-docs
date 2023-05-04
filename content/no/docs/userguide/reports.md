---
title: "Rapporter"
description: "En brukerveiledning for arbeid med rapporter"
lead: "En brukerveiledning for arbeid med rapporter."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 4
toc: true
---
Denne delen handler om å opprette og oppdatere `rapporter`.

Å klikke på `rapporter` gir tilgang til listen over tilgjengelige rapporter.

Rapporter lar deg bygge rapporter av data i `Q` som kan brukes til å overvåke og rapportere om statistikk for innsamlede data.

Det er to kategorier av rapporter i systemet.

| Type | Beskrivelse |
| --- | --- |
| `Normale rapporter` | Normale rapporter består av grafer og forhåndsdefinerte hermetiske grafer. |
| `Risikorapporter` | Risikorapporter består av risikorapportelementer. |

> Alle rapporter oppdateres når du endrer `avdeling` i navigatoren, slik at du kan bore ned i dataene og sammenligne data på tvers av avdelinger.

## Liste over sakerapporter

{{< zoomableImage src="/images/reports/reports_1_no.png" caption="Liste over sakerapporter" width="1600" height="600px">}}

Å klikke på `Sakerapport`-lenken tar deg til listen over `Sakerapporter` i systemet.

### Forhåndsvisning
{{< zoomableImage src="/images/reports/reports_2_no.png" caption="Forhåndsvisning av sakerapport" width="1600" height="600px">}}

Å klikke på `Forhåndsvisning` (øyesymbolet) i listen vil vise en forhåndsvisning av rapporten i skrivebeskyttet modus.

{{< zoomableImage src="/images/reports/reports_15_no.png" caption="Zoom inn på resultater" width="1600" height="600px">}}

Å klikke på `Zoom inn på resultater`-ikonet vil vise den komplette listen over alle dataene som er knyttet til grafkomponenten, slik at du kan utforske sakene som utgjør dataene.

{{< zoomableImage src="/images/reports/reports_16_no.png" caption="Detaljer om grafsegment" width="1600" height="600px">}}

Å klikke på et av segmentene i stolpediagrammet vil zoome inn og vise bare sakene som utgjør den stolpen.

### Redigering av rapport

{{< zoomableImage src="/images/reports/reports_3_no.png" caption="Redigering av rapport" width="1600" height="600px">}}

Når du redigerer eller oppretter en ny rapport, må du oppgi et `Rapportnavn` før du lagrer. Du kan også angi en beskrivelse for rapporten og legge til merkelapper for å gruppere rapporter etter nøkkelord.

Å legge til elementer i grafen lar deg bygge en graf som representerer flere analytiske komponenter.

Det er to hovedtyper av rapporter.

| Type | Beskrivelse |
| --- | --- |
| `Generell graf` | En generell rapportelementgraf. |
| `Forhåndsdefinerte grafer` | Forhåndsdefinerte rapporter som tillater spesifikke rapportelementer. |

{{< zoomableImage src="/images/reports/reports_4_no.png" caption="Generelle grafalternativer" width="1600" height="600px">}}

Når du redigerer eller legger til et nytt element i en rapport, har du følgende alternativer for en `Generell graf`.

| Alternativ | Beskrivelse |
| --- | --- |
| `Rediger filtre` | Rediger filtrene som brukes for å begrense dataene som brukes i grafen. |
| `Rapporttype` | Lar brukeren bytte mellom en `Generell graf` eller `Forhåndsdefinert graf`. |
| `Sakstype` | Velg hvilken type sak du vil bruke for grafen: `Melding`, `Handling` eller `Dokument`. |
| `Grupper etter` | Velg feltet å gruppere etter. |
| `Stable etter` | Velg et felt å stable etter. `Status`, `Prioritet`, `Kategori`, `Kategorigruppe` eller `Skjema`. Tilgjengelige felt avhenger av valgt `Sakstype`. |

{{< zoomableImage src="/images/reports/reports_6_no.png" caption="Redigering av filtre" width="1600" height="600px">}}

Å redigere filtrene vil føre til at en sidemeny dukker opp, der brukeren kan endre filtrene som brukes for å skjære og dele dataene for grafen.

{{< zoomableImage src="/images/reports/reports_7_no.png" caption="Forhåndsdefinerte grafer" width="1600" height="600px">}}

Hvis du velger alternativet `Forhåndsdefinerte grafer` fra rullegardinlisten `Rapporttype`, vil du se et skjema som vist ovenfor. Avhengig av typen `Forhåndsdefinert graf`, vil brukeren ha alternativer tilgjengelig for å justere resultatene av rapportelementet. De tilgjengelige `Forhåndsdefinerte grafer` er:

| Forhåndsdefinert graf | Beskrivelse |
| --- | --- |
| `Gjennomsnittlig syklus- og ledetid` | Mål syklus- og ledetid over et tidsvindu med løpende gjennomsnitt. Se definisjon av `Syklus` og `Ledetid` nedenfor. |
| `Saker etter saksstatusgruppe` | Antall saker over tid etter saksstatusgruppe. |
| `Saker etter saksstatus` | Antall saker over tid etter saksstatus.|
| `Ubearbeidede vs åpne og lukkede saker` | Antall ubearbeidede, åpne og lukkede saker over tid. |
| `Tid brukt i saksstatusgruppe etter persentil` | Tiden en sak tilbringer i hver saksstatusgruppe (ved å sette persentilen; for definisjon av persentil, se nedenfor). |
| `Tid brukt i saksstatus etter persentil` | Tiden en sak tilbringer i hver saksstatus (ved å sette persentilen; for definisjon av persentil, se nedenfor). |
| `Kumulativt antall saker etter avdeling` | Kumulativt antall saker per avdeling. |
| `Kumulative kostnader for saker etter avdeling` | Kumulative kostnader for saker per avdeling. |

#### Definisjoner
> Syklustid refererer til den gjennomsnittlige tiden det tar å fullføre en enkelt enhet. Ledetid refererer til tiden det tar fra mottak av en ordre til leveringsdatoen.
>
> Persentil uttrykkes som prosentandelen av verdiene i et sett med datapoeng som faller under en gitt verdi. Det vil si at hvis du setter persentilen til 90% og du får en verdi på 100, betyr det at 90% av resultatene i datasettet ditt faller under 100.

## Liste over risikorapporter

{{< zoomableImage src="/images/reports/reports_9_no.png" caption="Liste over risikorapporter" width="1600" height="600px">}}

Å klikke på `Risikorapport`-lenken tar deg til listen over `Risikorapporter` i systemet. Risikorapporter er rapporter som rapporterer mot en spesifisert `Risikomodell`, noe som lar oss bore ned i `Meldinger` som har risikokategorigrupper knyttet til dem.

Å klikke på `Forhåndsvisning`-knappen for en `Risikorapport` vil vise forhåndsvisningen av rapporten.

### Forhåndsvisning

{{< zoomableImage src="/images/reports/reports_8_no.png" caption="Forhåndsvisning av risikorapport" width="1600" height="600px">}}

Å klikke på boksene i den gjengitte risikomodellen tar deg direkte til sakene som er knyttet til faktorene i risikomodellen, slik at du kan undersøke de tilknyttede sakene innen den spesifikke rapporten.

### Redigering av rapport

{{< zoomableImage src="/images/reports/reports_11_no.png" caption="Redigering av risikorapport" width="1600" height="600px">}}

Når du redigerer eller oppretter en ny rapport, må du oppgi et `Rapportnavn` før du lagrer. Du kan også sette en beskrivelse for rapporten og legge til stikkord for å gruppere rapporter etter nøkkelord.

Å legge til elementer i grafen lar deg bygge en graf som representerer flere risikoanalysekomponenter.

{{< zoomableImage src="/images/reports/reports_13_no.png" caption="Legg til risikoelement: Risikomodell" width="1600" height="600px">}}

Ser vi på grensesnittet for `Legg til risikoelement`, kan vi se følgende alternativer når `Graf / Risikomodell-velgeren` er satt til `Risikomodell`.

| Alternativ | Beskrivelse |
| --- | --- |
| `Graf / Risikomodell-velger` | Bytt mellom graf- eller risikomodellvisning. |
| `Rediger filtre` | Juster filtrene for å filtrere ned resultatene. |
| `Risikomodell` | Velg risikomodellen som skal brukes for grafen. |

{{< zoomableImage src="/images/reports/reports_14_no.png" caption="Legg til risikoelement: Graf" width="1600" height="600px">}}

Ser vi på grensesnittet for `Legg til risikoelement`, kan vi se følgende alternativer når `Graf / Risikomodell-velgeren` er satt til `Graf`.

| Alternativ | Beskrivelse |
| --- | --- |
| `Graf / Risikomodell-velger` | Bytt mellom graf- eller risikomodellvisning. |
| `Rediger filtre` | Juster filtrene for å filtrere ned resultatene. |
| `Risikomodell` | Velg risikomodellen som skal brukes for grafen. |
| `Grupper etter` | Grupper etter felt: `Avdeling`, `Status`, `Prioritet`, `Kategori`, `Kategorigruppe`, `Skjema`, `År`, `Måned`, `Dato` eller `Risikonivå`. |
| `Stable etter` | Stable etter følgende felt: `Status`, `Prioritet`, `Kategori`, `Kategorigruppe`, `Skjema` eller `Risikonivå`. |
| `Visningstype` | Velg visningstype: enten `Antall saker` eller `Feilkostnad`. |