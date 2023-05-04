---
title: "Sakstavle"
description: "En brukerveiledning for å jobbe med sakstavler"
lead: "En brukerveiledning for å jobbe med sakstavlene. Vi dekker hvordan man oppretter, oppdaterer og administrerer sakstavler."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 2
toc: true
---
Denne delen omhandler bruk av Sakstavlen.

Når du klikker på `Sakstavle`, får du tilgang til Sakstavle-grensesnittet.

## Sakstavlen

{{< zoomableImage src="/images/case_board/case_board_1_no.png" caption="Oversikt over sakstavle" width="1600" height="600px">}}

Sakstavlen gir en brukervennlig og effektiv måte å administrere saker innenfor ulike arbeidsflyter. Det lar deg enkelt flytte saker mellom status, filtrere tavlen ved hjelp av ulike kriterier og få tilgang til saksinformasjon.

| Valg | Beskrivelse |
| --- | --- |
| `Velg arbeidsflyt` | Velg blant arbeidsflytene du har tilgang til, slik at du kan bytte mellom ulike sakstavler. |
| `Sakstatus` | Arbeidsflyt-sakstatusene vises som kolonner, med saker gruppert etter deres respektive status. Et unntak er `Lukk`-kolonnen for sakstatus, der sakene er gruppert etter uke for å forhindre informasjonsoverbelastning. |
| `Skjul/Utvid kolonnen` | Brukere kan skjule eller utvide kolonner for å redusere informasjonstettheten på skjermen. |
| `Sak` | Hver boks representerer en aktiv sak i systemet. Brukere kan klikke på en sak for å få en rask oversikt over detaljene. ...-menyen på sakboksen gir tilgang til en meny som viser statusene saken kan overføres til. |
| `Søk` | Søkeboksen i øverste høyre hjørne lar deg filtrere saker som er synlige på tavlen ved å søke i titlene og beskrivelsene av tilgjengelige saker.|

### Sakstatusovergang

{{< zoomableImage src="/images/case_board/case_board_6_no.png" caption="Overgang mellom tilstander" width="1600" height="600px">}}

For å flytte saker, klikk og dra enkelt en sak til en ny statuskolonne.

{{< zoomableImage src="/images/case_board/case_board_3_no.png" caption="Utfylling av en dialogboks ved overgang mellom tilstander" width="1600" height="600px">}}

Hvis det kreves å fylle ut en dialogboks for å flytte en sak fra gjeldende status til en ny status, vil den dukke opp og må fylles ut før saken kan flyttes til den nye statusen.

{{< zoomableImage src="/images/case_board/case_board_5_no.png" caption="Overgang mellom status ved hjelp av hamburgermenyen" width="1600" height="600px">}}

Alternativt kan du flytte en sak ved å klikke på hamburgermenyen i øvre høyre hjørne av hver sakboks og deretter velge en av de tillatte statusovergangene.

### Visning av saksinformasjon

{{< zoomableImage src="/images/case_board/case_board_4_no.png" caption="Vis kompakt saksoversikt" width="1600" height="600px">}}

Ved å klikke på en sak i sakstavlen, kan du få tilgang til `kompakt saksoversikt`. For en mer detaljert oversikt, klikk på pilikonet i øvre høyre hjørne av `kompakt saksoversikt` for å åpne full saksoversikt. `Kompakt saksoversikt` tilbyr flere nyttige alternativer:

| Valg | Beskrivelse |
| --- | --- |
| `Tittel` | Brukere kan klikke direkte på tittelen for å redigere den, og tilpasse saksnavnet etter behov. |
| `Beskrivelse` | Brukere kan redigere saksbeskrivelsen og klikke på `Lagre`-knappen for å lagre endringene. |
| `Kommentar` | Kommentarseksjonen lar brukerne raskt legge til en kommentar i saken. Ved å klikke på `Varsle`-knappen, kan brukere velge hvilke personer de vil varsle om den nye kommentaren. Når det er valgt, klikk på `Kommentar` for å lagre kommentaren i saken og sende varsler til de valgte mottakerne. |
| `Saksbehandler` | Brukere kan tilordne eller endre nåværende saksbehandler som er ansvarlig for å håndtere saken. |
| `Saksgodkjenner` | Brukere kan tilordne eller endre nåværende saksgodkjenner som er ansvarlig for å godkjenne saksbeslutninger. |
| `Sakstatus` | Brukere kan endre sakstatusen for å gjenspeile dens nåværende tilstand i arbeidsflyten. |
| `Avdeling` | Brukere kan oppdatere sakens tilknyttede avdeling for å sikre nøyaktig kategorisering. |
| `Prioritet` | Brukere kan endre saksprioritetsnivået for å indikere dens relative betydning eller hastegrad. |
| `Oppgaver` | `Oppgaver`-alternativet viser alle ventende oppgaver knyttet til saken, og lar brukere vise og endre statusen for hver oppgave etter behov. |

## Avanserte Sakstavle-filtre

Sakstavlen gir et brukervennlig grensesnitt for å håndtere og organisere saker effektivt. Den utskyvbare alternativmenyen som ligger på venstre side av skjermen, lar brukere filtrere sakstavlen basert på spesifikke krav. Denne menyen inneholder flere forhåndsdefinerte filtre, som hver tjener et annet formål.

Følgende tabell viser de forhåndsdefinerte filtrene og deres beskrivelser:

| Forhåndsdefinert filter      | Beskrivelse                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------|
| `Håndtert av meg`         | Viser saker tildelt den nåværende innloggede brukeren som saksbehandler.                      |
| `Godkjent av meg`        | Viser saker der den nåværende innloggede brukeren fungerer som saksgodkjenner.                |
| `Deltatt i av meg` | Viser saker der den nåværende innloggede brukeren deltar som en sakdeltaker.                  |
| `Ingen saksbehandler`       | Viser saker uten en tildelt saksbehandler.                                                    |
| `Ingen saksgodkjennere`     | Viser saker uten en tildelt saksgodkjenner.                                                   |
| `Ingen oppgaver`              | Viser saker som ikke har noen tilknyttede oppgaver.                                           |
| `Forsinket`               | Viser saker som er forsinket.                                                                 |
| `Oppdatert i dag`         | Viser saker som er oppdatert på den nåværende dagen.                                          |
| `Oppdatert siste uke`  | Viser saker som er oppdatert i løpet av den siste uken.                                       |
| `Opprettet i dag`         | Viser saker som er opprettet på den nåværende dagen.                                          |
| `Opprettet siste uke`  | Viser saker som er opprettet i løpet av den siste uken.                                       |

I tillegg til de forhåndsdefinerte filtrene, er det flere andre filtre tilgjengelig for bruk. Disse filtrene kan variere avhengig av arbeidsflyttypen (for eksempel melding, handling, dokument, høring eller revisjon av arbeidsflyt).

Følgende tabell presenterer disse ekstra filtrene, deres gjeldende enhetstyper og beskrivelser:

| Filter          | Enhetstyper | Beskrivelse                                                                                                                  |
|-----------------|--------------|------------------------------------------------------------------------------------------------------------------------------|
| `Saksgodkjennere`| `Alle`        | Lar brukere legge til saksgodkjenner(e) i filteret. Saker med minst en av de angitte godkjennerne vil bli vist.  |
| `Saksbehandler`  | `Alle`        | Lar brukere legge til saksbehandler(e) i filteret. Saker med minst en av de angitte saksbehandlerne vil bli vist.     |
| `Sakskategori` | `Melding`    | Hjelper brukere med å finne saker som inneholder en eller
