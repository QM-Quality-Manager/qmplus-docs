---
title: "Dashboards"
description: "A user guide for working with dashboards"
lead: "A user guide for working with dashboards. We cover how to create and modify dashboards."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 1
toc: true
---
Denne delen fokuserer på å administrere brukerdashbord.

Ved å klikke på `Dashboards` får du tilgang til listen over en brukers dashbord.

## Oversikt

Dashbord er samlinger av komponenter som er designet for å overvåke statusen til plattformen. Du kan opprette dashbord for spesifikke mål eller for å vise bestemt informasjon. Det finnes to typer dashbord.

| Type | Beskrivelse |
| --- | --- |
| `User` | Dashbord som brukere kan opprette selv, ved hjelp av tilgjengelige komponenter. |
| `User Type` | Skrivebeskyttede dashbord opprettet for bestemte brukertyper. Disse dashbordene brukes til å dele fast informasjon blant alle brukere av en viss brukertype og kan bidra til å sikre at alle rapporterer samme data. |

### Konfigurer brukertype-dashbord

{{< figure src="/images/dashboards/dashboards_22_no.png" caption="Liste over brukertyper" width="1024">}}

For å opprette eller endre `User Type` dashbord, naviger først til listen over `User Types`. Klikk på en av `User Types` for å åpne `User Type`, og klikk deretter på fanen `Dashboards`.

{{< figure src="/images/dashboards/dashboards_23_no.png" caption="Brukertype-dashbord" width="1024">}}

Dashbord som konfigureres her, vil vises for brukere av den `User Type` når de klikker på menyvalget `Dashboards`.

## Dashbord

{{< figure src="/images/dashboards/dashboards_1_no.png" caption="Eksempel på et dashbord med konfigurerte komponenter" width="1024">}}

Over er et eksempel på et dashbord med noen konfigurerte komponenter.

{{< figure src="/images/dashboards/dashboards_2_no.png" caption="Typer av dashbord" width="1024">}}

Det finnes to typer dashbord.

| Type | Beskrivelse |
| --- | --- |
| `Brukertype` | Et skrivebeskyttet dashbord spesifisert for den påloggede brukerens brukertype. Kan brukes for å sikre ensartet rapportering av tall og status. |
| `Bruker opprettet` | Et dashbord opprettet av den påloggede brukeren. |

{{< figure src="/images/dashboards/dashboards_5_no.png" caption="Velge antall kolonner i et dashbord" width="1024">}}

Ved å klikke på symbolet `Kolonner`, kan du justere antall kolonner som brukes til å vise dashbordet, noe som gir mer nøyaktig kontroll over komponentoppsettet.

{{< figure src="/images/dashboards/dashboards_4_no.png" caption="Konfigurer dashbordsidefelt" width="1024">}}

Ved å klikke på knappen `Konfigurere` på dashbordet, får du tilgang til lagrede eksisterende komponenter som kan gjenbrukes. Disse komponentene kommer i to typer.

| Type | Beskrivelse |
| --- | --- |
| `Generell` | Komponenter som deles på tvers av hele organisasjonen og er tilgjengelige for alle brukere å opprette. Brukeren må ha tillatelse til å opprette generelle komponenter for å kunne lage nye komponenter her. |
| `Mine komponenter` | Komponenter som den påloggede brukeren allerede har opprettet og som kun er synlige for dem. |

## Komponenter

{{< figure src="/images/dashboards/dashboards_3_no.png" caption="Tilgjengelige komponenttyper" width="1024">}}

Det er flere komponenter tilgjengelige for å legge til i et dashbord. Disse kan brukes til å lage informasjonsdashbord for sluttbrukere eller for deg selv.

### Diagram

{{< figure src="/images/dashboards/dashboards_8_no.png" caption="Diagramkomponent" width="1024">}}

Diagrammer lar deg opprette komponenter som visualiserer data lagret i `Q`. La oss se på de tilgjengelige alternativene.

| Alternativ | Beskrivelse |
| --- | --- |
| `Komponentnavn` | Angi navnet på komponenten, med støtte for flere språk. |
| `Sakstype` | Velg sakstypen for grafen. Dette kan være `Melding`, `Tiltak`, `Dokument`, `Høring`, eller `Revisjon`. |
| `Visningstype` | Velg visningstypen for grafen. Dette kan være en `Linjediagram`, `Arealdiagram`, `Stolpediagram`, eller `Kake diagram`. |
| `Stable etter` | Aktiver/deaktiver stable etter-feltalternativet for grafen. |
| `Stabelfelt` | Velg feltet å stable etter. Se tabellen nedenfor. |
| `X-aksen` | Velg alternativene for x-aksen (x-akse og y-akse kan byttes om). |
| `Y-aksen` | Velg alternativene for y-aksen (x-akse og y-akse kan byttes om). |
| `Periode` | Velg tidsperioden for grafdataene. De tilgjengelige feltene avhenger av sakstypen. |
| `Filtre` | Legg til, fjern og endre filtre for å begrense resultatene som returneres for grafen. |
| `Overstyr uttrykk` | Lar sluttbrukeren overstyre spørrespråket som kjører mot `Q`-apiet. |
| `Overstyr visuelle spesifikasjoner` | Aktiverer sluttbrukeren til å overstyre VegaLite-grafdefinisjonen som brukes til å vise grafen. |

{{< figure src="/images/dashboards/dashboards_24_no.png" caption="Tilgjengelige stack by-felt" width="1024">}}

De tilgjengelige stack by-feltene er:

| Felt | Beskrivelse |
| --- | --- |
| `Prioritet` | Stable etter prioritet for saken. |
| `Saksstatus` | Stable etter saksstatus for saken. |
| `Avdeling` | Stable etter avdeling for saken. |
| `Skjema` | Stable etter skjema for saken. |

### Kart

{{< figure src="/images/dashboards/dashboards_11_no.png" caption="Kartkomponent" width="1024">}}

Kartkomponenten lar deg lage en spørring som vil bli kartlagt til et karteksempel hvis meldingssaken har tilknyttede geokoordinater.

### Tabell

{{< figure src="/images/dashboards/dashboards_1_no.png" caption="Tabellvisningskomponent" width="1024">}}

Tabellkomponenten er en liste-komponent som viser resultatene av en bestemt spørring. Her er en oversikt over alternativene:

| Alternativ | Beskrivelse |
| --- | --- |
| `Komponentnavn` | Angi navnet på komponenten, med støtte for flere språk. |
| `Sakstype` | Velg sakstypen for grafen. Dette kan være `Melding`, `Tiltak`, `Dokument`, `Høring`, eller `Revisjon`. |
| `Kolonner` | Velg kolonnene som skal vises i listen med resultater. |
| `Antall` | Velg antall oppføringer per side i listen. |
| `Periode` | Velg datoperioden for oppføringene i listen. |
| `Filtre` | Legg til, fjern og oppdater filtre for spørringen. |
| `Overstyr uttrykk` | Overstyr den nåværende genererte uttrykket. |

### Forhåndsdefinerte grafer

{{< figure src="/images/dashboards/dashboards_13_no.png" caption="Forhåndsdefinerte grafer-komponent" width="1024">}}

Forhåndsdefinerte grafer er ferdiglagde (hermetiske) rapporter som du kan bruke for å målrette spesifikke analytiske mål. La oss se på feltene i sidepanelet.

| Felt | Beskrivelse |
| --- | --- |
| `Komponentnavn` | Angi navnet på komponenten, med støtte for flere språk. |
| `Graftype` | Velg den forhåndsdefinerte graf-typen, se tabellen nedenfor. |
| `Filtre` | Et sett med filtre som vil variere avhengig av den forhåndsdefinerte graf-typen brukeren velger. |
| `Periode` | Velg data for rapporten etter tidsperiode. |
| `Overstyr uttrykk` | Aktiver/deaktiver muligheten til å overstyre uttrykket som sendes til `Q`. |

De tilgjengelige forhåndsdefinerte grafene er:

| Forhåndsdefinert graf | Beskrivelse |
| --- | --- |
| `Gjennomsnittlig syklus og ledetid` | Mål syklus- og ledetid over et løpende gjennomsnittsvindu. Se definisjonen av `Syklus` og `Lede` tid nedenfor. |
| `Sak for sak statusgruppe` | Antall saker over tid etter saksstatusgruppe. |
| `Saker for saksstatus` | Antall saker over tid etter saksstatus. |
| `Ubehandlede vs åpne og lukkede saker` | Antall saker ubehandlet, åpne og lukkede over tid. |
| `Tid brukt i saksstatusgruppe etter persentil` | Tid en sak tilbringer i hver sakstatusgruppe (innstilling av persentil, for definisjon av persentil, se nedenfor). |
| `Tid brukt i saksstatus etter persentil` | Tid en sak tilbringer i hver sakstatus (innstilling av persentil, for definisjon av persentil, se nedenfor). |
| `Akkumulert antall saker etter avdeling` | Kumulativt antall saker per avdeling. |
| `Akkumulerte kostnader for saker etter avdeling` | Kumulative kostnader for saker per avdeling. |

#### Definisjoner
> Syklustid refererer til den gjennomsnittlige tiden det tar å fullføre en enkelt enhet. Ledetid refererer til lengden på tid det tar fra datoen for mottak av en ordre til leveringsdatoen.
>
> Persentil, uttrykt som prosentandelen av verdier i et sett med data som faller under en gitt verdi. Det vil si at hvis du setter persentilen til 90% og får en verdi på 100, betyr det at 90% av resultatene i datasettet ditt faller under 100.

#### **Syklus- og ledetid Løpende gjennomsnitt** Filtre
{{< figure src="/images/dashboards/dashboards_25_no.png" caption="Syklus- og ledetidgraf" width="1024">}}

Filtrene som er tilgjengelige for den forhåndsdefinerte graf-typen `Syklus- og ledetid Løpende gjennomsnitt` er:

| Felt | Beskrivelse |
| --- | --- |
| `Arbeidsflyt` | Velg arbeidsflyten du vil rapportere om. |
| `Kategorigruppe` | Velg kategorigruppen du ønsker å bruke for å filtrere resultatene. |
| `Kategori` | Velg kategorien i kategorigruppen som skal brukes for filtrering. |
| `Størrelsen på det rullende vinduet i dager` | Størrelsen på det rullende vinduet (vi anbefaler 7 dager). |

#### **Saker etter sakstatusgruppe** Filtre
{{< figure src="/images/dashboards/dashboards_26_no.png" caption="Saker etter sakstatusgruppegraf" width="1024">}}

Filtrene som er tilgjengelige for den forhåndsdefinerte graf-typen `Saker etter sakstatusgruppe` er:

| Felt | Beskrivelse |
| --- | --- |
| `Arbeidsflyt` | Velg arbeidsflyten du vil rapportere om. |
| `Kategorigruppe` | Velg kategorigruppen du ønsker å bruke for å filtrere resultatene. |
| `Kategori` | Velg kategorien i kategorigruppen som skal brukes for filtrering. |

#### **Saker etter sakstatus** Filtre
{{< figure src="/images/dashboards/dashboards_27_no.png" caption="Saker etter sakstatusgraf" width="1024">}}

Filtrene som er tilgjengelige for den forhåndsdefinerte graf-typen `Saker etter sakstatus` er:

| Felt | Beskrivelse |
| --- | --- |
| `Arbeidsflyt` | Velg arbeidsflyten du vil rapportere om. |
| `Kategorigruppe` | Velg kategorigruppen du ønsker å bruke for å filtrere resultatene. |
| `Kategori` | Velg kategorien i kategorigruppen som skal brukes for filtrering. |

#### **Ubehandlet vs Åpne og Lukkede saker** Filtre
{{< figure src="/images/dashboards/dashboards_28_no.png" caption="Ubehandlet vs Åpne og Lukkede saker graf" width="1024">}}

Filtrene som er tilgjengelige for den forhåndsdefinerte graf-typen `Ubehandlet vs Åpne og Lukkede saker` er:

| Felt | Beskrivelse |
| --- | --- |
| `Arbeidsflyt` | Velg arbeidsflyten du vil rapportere om. |
| `Kategorigruppe` | Velg kategorigruppen du ønsker å bruke for å filtrere resultatene. |
| `Kategori` | Velg kategorien i kategorigruppen som skal brukes for filtrering. |

#### **Tid brukt i sakstatusgruppe etter persentil** Filtre
{{< figure src="/images/dashboards/dashboards_29_no.png" caption="Tid brukt i hver sakstatusgruppe etter persentilgraf" width="1024">}}

Filtrene som er tilgjengelige for den forhåndsdefinerte graf-typen `Tid brukt i sakstatusgruppe etter persentil` er:

| Felt | Beskrivelse |
| --- | --- |
| `Arbeidsflyt` | Velg arbeidsflyten du vil rapportere om. |
| `Kategorigruppe` | Velg kategorigruppen du ønsker å bruke for å filtrere resultatene. |
| `Kategori` | Velg kategorien i kategorigruppen som skal brukes for filtrering. |
| `Persentil` | Persentilen som brukes til å beregne tiden brukt. |

#### **Tid brukt i sakstatus etter persentil** Filtre
{{< figure src="/images/dashboards/dashboards_30_no.png" caption="Tid brukt i hver sakstatus etter persentilgraf" width="1024">}}

Filtrene som er tilgjengelige for den forhåndsdefinerte graf-typen `Tid brukt i sakstatus etter persentil` er:

| Felt | Beskrivelse |
| --- | --- |
| `Arbeidsflyt` | Velg arbeidsflyten du vil rapportere om. |
| `Kategorigruppe` | Velg kategorigruppen du ønsker å bruke for å filtrere resultatene. |
| `Kategori` | Velg kategorien i kategorigruppen som skal brukes for filtrering. |
| `Persentil` | Persentilen som brukes til å beregne tiden brukt. |

#### **Kumulativt antall saker per avdeling** Filtre
{{< figure src="/images/dashboards/dashboards_31_no.png" caption="Kumulativt antall saker" width="1024">}}

Det er ingen filtre tilgjengelige for den forhåndsdefinerte grafen `Kumulativt antall saker per avdeling`.

#### **Kumulativ kostnad for saker per avdeling** Filtre
{{< figure src="/images/dashboards/dashboards_32_no.png" caption="Kumulativ kostnad for saker" width="1024">}}

Det er ingen filtre tilgjengelige for den forhåndsdefinerte grafen `Kumulativ kostnad for saker per avdeling`.

### Mine saker

{{< figure src="/images/dashboards/dashboards_14_no.png" caption="Innloggede brukeres saker" width="1024">}}

Komponenten `Mine saker` gir deg informasjon relatert til den nåværende innloggede brukeren. Det er tre faner.

| Fane | Beskrivelse |
| --- | --- |
| `Meldinger jeg rapporterte` | Meldinger jeg la inn på plattformen. |
| `Mine saker som saksbehandler` | Alle sakene jeg er tildelt som saksbehandler. |
| `Mine oppgaver` | Alle mine tildelte oppgaver i saker. |

### Mine aktiviteter

{{< figure src="/images/dashboards/dashboards_15_no.png" caption="Innloggede brukeres aktiviteter" width="1024">}}

Komponenten `Mine aktiviteter` viser alle kommende aktiviteter knyttet til den nåværende innloggede brukeren. Brukere kan få direkte tilgang til en gitt aktivitet ved å klikke på lenken for hver rad.

### Eskalerte saker

{{< figure src="/images/dashboards/dashboards_16_no.png" caption="Eskalerte saker komponent" width="1024">}}

Komponenten `Eskalerte saker` viser alle sakene som har blitt eskalert av systemet innenfor perioden som er spesifisert i filtrene. Dette lar den innloggede brukeren se og arbeide med eskalerte saker.

### Dokumentoppdateringer

{{< figure src="/images/dashboards/dashboards_17_no.png" caption="Komponenter for oppdaterte dokumenter" width="1024">}}

Komponenten `Dokumentoppdateringer` gjør det mulig for den innloggede brukeren å se hvilke dokumenter som har blitt oppdatert innenfor perioden spesifisert av filtrene i komponentinnstillingene. For eksempel kan dette vise alle oppdaterte dokumenter de siste 7 dagene.

### Favorittdokumenter

{{< figure src="/images/dashboards/dashboards_19_no.png" caption="Favorittdokumenter komponent" width="1024">}}

Komponenten `Favorittdokumenter` viser alle dokumentene som er favorisert av den nåværende innloggede brukeren.

### Integrert dokumentvisning

{{< figure src="/images/dashboards/dashboards_20_no.png" caption="Legg til integrerte dokumenter på instrumentbordet" width="1024">}}

Komponenten `Integrert dokumentvisning` lar deg legge inn et dokument direkte på instrumentbordet som visbart innhold. Følgende typer dokumenttyper støttes:

| Type | Beskrivelse |
| --- | --- |
| `Tekstdokument` | Et HTML-lignende dokument som vises i komponenten. |
| `Prosessdiagram` | Et prosessdiagramdokument gjengitt i komponenten. |
| `Rik tekst` | Et skrivebeskyttet rikt tekst-dokument lagret i `Q`. |
| `Regneark` | Et skrivebeskyttet regneark lagret i `Q`. |

> Alle `Integrerte dokumenter` er `KUN LESE` og kan ikke redigeres.