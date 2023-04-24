---
title: "Administrator/Kategorier"
description: "En brukerveiledning for arbeid med kategorigrupper"
lead: "En brukerveiledning for arbeid med kategorigrupper. Vi dekker hvordan du oppretter og endrer kategorigrupper."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 11
toc: true
---
Denne seksjonen omhandler administrasjon av kategorigrupper i systemet.

Ved å klikke på `Administrator/Kategorier` får du tilgang til listen over kategorigrupper.

En kategorigruppe består av en trestruktur med `underkategorigrupper` og `kategorier`. Brukere kan organisere disse elementene i den rekkefølgen de ønsker.

> Kategorigrupper kan gjenbrukes på tvers av flere skjemaer, noe som lar deg generere statistikk og rapporter fra ulike skjemaer for sammenligning.

Det er viktig å merke seg at alle `Kategorigrupper` er versjonert. Dette gjør at du kan endre en kategorigruppe uten å påvirke eksisterende skjemaer som inneholder den aktuelle kategorigruppen.

## Liste over kategorigrupper

{{< figure src="/images/category_groups/category_group_10_no.png" caption="Listevisning av kategorigrupper" width="1024">}}

Listevisningen av kategorigrupper lar deg se alle kategorigruppene i systemet og filtrere dem etter flere parametere, inkludert kategorigruppens navn og synlighet.

{{< figure src="/images/category_groups/category_group_1_no.png" caption="Tilgang til filtre for kategorigruppelisten" width="1024">}}

For å få tilgang til ytterligere filtre, klikk på filterknappen og velg alternativer fra sidepanelet.

## Opprett kategorigruppe

{{< figure src="/images/category_groups/category_group_9_no.png" caption="Oppretting av en ny kategorigruppe" width="1024">}}

Når du oppretter en kategorigruppe, har du følgende felter tilgjengelig:

| Felt | Beskrivelse |
| --- | --- | 
| `Kategorigruppetittel` | Kategorigruppens navn med støtte for flere språk, slik at du kan tilby oversettelser for andre språk som brukes i organisasjonen. |
| `Gruppetype` | Typen kategorigruppe som opprettes. Se beskrivelsen nedenfor. |
| `Synlighet` | Angir kategorigruppens synlighet i organisasjonen. For eksempel vil å sette dette til `avdeling` gjøre kategorigruppen synlig bare for den valgte avdelingen.|
| `Avdeling` | Velg avdelingen som denne kategorigruppen skal registreres til. Sammen med `synlighet` styrer dette kategorigruppens synlighet. |
| `Kategorier` | Hovedaspektet som lar deg legge til `underkategorigrupper` og `kategorier`, og lage en `tre-lignende` struktur med nøstet informasjon. |
| `Referanse` | Lar deg angi en `dokument`-referanse som vises sammen med kategorigruppen i skjemaer, for eksempel å lenke til en relevant lov. Dette kan også gjøres for underkategorigrupper og kategorier som legges til. |

`Gruppetype` lar deg angi hvilken type kategorigruppe du oppretter. Alternativene er:

| Gruppetype | Beskrivelse |
| --- | --- |
| `Definerende` | En spesiell `Enkeltvalg` kategorigruppe som brukes som en `definerende` kategorigruppe i et skjema. Lar sluttbrukere velge `kun én` kategori som svar. |
| `Enkeltvalg` | Lar brukere velge én `kategori` når de legger inn data i et skjema. |
| `Flervalg` | Lar brukere velge flere `kategorier` når de legger inn data i et skjema. |
| `Tiltak` | Lar brukere velge én `kategori` for en handling. Denne kategorigruppen er forskjellig fra `Enkeltvalg` kun i at den er merket som en `handling`-gruppe. |
| `Nummer` | Lar brukere legge inn numeriske verdier for alle kategorier i gruppen. Dette kan brukes til å samle inn valutanummer eller annen informasjon. |
| `Risiko` | Lar brukere legge inn risikoanalyseverdier for en gitt tilknyttet risikomodell. |

> Hvis du velger gruppetype `Risiko`, vil et ekstra felt vises i skjemaet for `Opprett kategorigruppe`, som lar deg velge `Risikomodellen` denne kategorigruppen vil være basert på.

Klikk på `Set risk model`-knappen for å vise sidepanelet der du kan velge den tilknyttede risikomodellen.

{{< figure src="/images/category_groups/category_group_11_no.png" caption="Klikk på knappen for å velge en risikomodell" width="1024">}}

Herfra kan du velge risikomodellen du vil bruke sammen med kategorigruppen.

{{< figure src="/images/category_groups/category_group_5_no.png" caption="Velg risikomodellen" width="1024">}}

Til slutt kan du velge et `referansedokument` som du ønsker å inkludere som en referanse i kategorigruppen.

### Legg til og rediger kategorigruppe

{{< figure src="/images/category_groups/category_group_8_no.png" caption="Oppretting av underkategorigruppe" width="1024">}}

For å opprette en `Underkategorigruppe` må du angi et navn for kategorigruppen. En valgfri beskrivelse kan også legges til. Til slutt kan du legge ved et referansedokument for `Underkategorigruppen`, som vil vises i skjemaer når undergruppen gjengis.

### Legg til og rediger kategori

{{< figure src="/images/category_groups/category_group_7_no.png" caption="Oppretting av ny kategori" width="1024">}}

Når du legger til en kategori i kategorigruppen, må følgende felter fylles ut:

| Felt | Påkrevd | Beskrivelse |
| --- | --- | --- |
| `Kategorinavn` | **X** | Angi navnet på kategorien som legges til (støtter flere språk). |
| `Beskrivelse` | | Valgfri beskrivelse for kategorien. |
| `Synlighet` | **X** | Angi standard synlighet for kategorien (hvilken avdeling den er synlig i). |
| `Avdeling` | **X** | Avdelingen der kategorien er synlig. |
| `Prioritet` | | Prioriteten som tildeles skjemainnlegget hvis kategorien er valgt. |
| `Kostnad` | | Kostnaden som påføres skjemainnlegget hvis kategorien er valgt. |
| `Referanse` | | Den valgfrie dokumentreferansen som vises når kategorien gjengis i et skjema. |

Til slutt, klikk på `Lagre endringer`-knappen for å lagre den nye kategorien i kategorigruppen.

{{< figure src="/images/category_groups/category_group_3_no.png" caption="Redigere en eksisterende kategori" width="1024">}}

Du kan også redigere en eksisterende kategori, akkurat som når du oppretter en ny.

### Organisere struktur

{{< figure src="/images/category_groups/category_group_6_no.png" caption="Organisering av kategorigruppen" width="1024">}}

For å organisere strukturen i kategorigruppen kan du dra elementer til ønsket rekkefølge.

> Dra kategorier til høyre under en kategorigruppe for å organisere dem under undergruppen.

Du kan også redigere, se kategoridetaljer eller slette kategorier/underkategorigrupper.

{{< figure src="/images/category_groups/category_group_4_no.png" caption="Se detaljer om en kategori" width="1024">}}

Dette er visningen når du klikker på `se kategoridetaljer`.

### Referanser

{{< figure src="/images/category_groups/category_group_2_no.png" caption="Legge til referanser i kategorigruppe" width="1024">}}

Referanser lar deg legge ved lenker til interne dokumenter som inneholder relevant informasjon om en bestemt kategorigruppe, kategori eller underkategorigruppe. Eksempler på dette inkluderer lenker til lover eller instruksjoner knyttet til en gitt oppføring.