---
title: "Administrator/Spørreskjemaer"
description: "En brukerveiledning for arbeid med spørreskjemaer"
lead: "En brukerveiledning for arbeid med spørreskjemaer. Vi dekker hvordan du oppretter og endrer spørreskjemaer."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 19
toc: true
---
Denne seksjonen fokuserer på å administrere spørreskjemaer i systemet.

Klikke på `Administrator/Spørreskjemaer` gir tilgang til listen over spørreskjemaer.

## Liste over spørreskjemaer

{{< zoomableImage src="/images/questionnaires/questionnaires_1_no.png" caption="Liste over spørreskjemaer" width="1600" height="600px">}}

Spørreskjemaer brukes til å lage omfattende spørreskjemaer og sjekklister som kan spenne over enten én side eller flere sider.

Du kan filtrere mellom `Aktive`, `Deaktive`, eller `Alle` status, søke etter tittel og sjekke om spørreskjemaet er publisert eller ikke.

## Opprette spørreskjema

### Generell fane

{{< zoomableImage src="/images/questionnaires/questionnaires_2_no.png" caption="Generell fane" width="1600" height="600px">}}

Å opprette et spørreskjema krever følgende felt.

| Felt | Beskrivelse |
| --- | --- |
| `Tittel` | Tittel på spørreskjemaet, støtter flere språk. |
| `Beskrivelse` | Valgfri beskrivelse for spørreskjemaet. |
| `Spørreskjema visningstype` | Hvordan spørreskjemaet skal vises (Enkelt side eller Flere sider). |
| `Synlighet` | Synligheten til spørreskjemaet. |
| `Avdeling` | Avdelingen der spørreskjemaet befinner seg. |
| `Referanse` | En eller flere dokumentreferanser knyttet til spørreskjemaet. |
| `Tags` | Legg til tagger på spørreskjemaet for å identifisere det. |

Som du kan se fra bildet, kan vi forhåndsvise det nåværende spørreskjemaet.

> Inntil du klikker på `Utgiver`-knappen, er alle endringer i spørreskjemaet private. Når `Utgiver`-knappen klikkes, vil det være synlig for å legge til aktiviteter.

{{< zoomableImage src="/images/questionnaires/questionnaires_7_no.png" caption="Dokumentreferanser" width="1600" height="600px">}}

Referanser kan legges til dokumenter lagret i `Q` for å gi kontekst til et spørreskjema eller relevante dokumenter.

## Spørreskjemaets utforming

{{< zoomableImage src="/images/questionnaires/questionnaires_8_no.png" caption="Spørreskjema-bygger" width="1600" height="600px">}}

Spørreskjema-byggeren har noen kjernbegreper å forstå. Et spørreskjema er en samling av en eller flere sider, der hver side har en eller flere kolonner med komponenter. Forhåndsvisningsknappen lar deg teste spørreskjemaet under utvikling. Ved å klikke på lagre-knappen vil du lagre en ny versjon av spørreskjemaet, og når det er klart, kan du klikke `Utgiver` for å frigi det nye spørreskjemaet for bruk.

> Alle spørreskjemainnganger er knyttet til en bestemt spørreskjemaversjon, noe som betyr at gamle data blir bevart korrekt mot en tidligere versjon av et spørreskjema.

{{< zoomableImage src="/images/questionnaires/questionnaires_4_no.png" caption="Tilgjengelige spørreskjemakomponenter" width="1600" height="600px">}}

De tilgjengelige komponentene er som følger.

| Komponent | Beskrivelse |
| --- | --- |
| `Tekst` | Et tekstbeskrivelsesfelt for å skrive inn tekstinformasjon i spørreskjemaet. |
| `Bilde` | Lar deg legge til et bilde i spørreskjemaet, kan brukes til å vise informasjon. |
| `Enkeltvalg` | Opprett et spørsmål med svar, slik at sluttbrukeren kan velge ett. |
| `Flervalg` | Opprett et spørsmål med svar, slik at sluttbrukeren kan velge flere. |
| `Rangering` | Opprett et spørsmål med svar, slik at sluttbrukeren kan dra og slippe dem i rangeringsrekkefølgen. |
| `Heltall` | Et felt som lar deg angi et helt tall. |
| `Desimal` | Et felt som lar deg angi et desimaltall. |
| `Valuta` | Et felt som lar deg angi et valutatall. |
| `Tall i område` | Et felt som lar deg angi en start- og sluttposisjon og trinnstørrelse for glidebryteren. |
| `Enlinjetekstfelt` | Et enkelt tekstlinjefelt. |
| `Flere linjers tekstfelt` | Et flerlinjet tekstfelt. |
| `Risiko` | En risikokategorigruppe. |

> Komponenter kan endres i størrelse horisontalt og flyttes rundt. Avhengig av antall kolonner du definerer, kan du organisere komponentene side om side.

### Sideinnstillinger

{{< zoomableImage src="/images/questionnaires/questionnaires_9_no.png" caption="Spørreskjema sideinnstillinger" width="1600" height="600px">}}

Sideinnstillingene lar deg endre sidetittelen og beskrivelsen. Du kan også legge til referanser til dokumenter fra Q og tagger.

### Tekst
{{< zoomableImage src="/images/questionnaires/questionnaires_12_no.png" caption="Tekstkomponent" width="1600" height="600px">}}

Et tekstfelt som lar deg angi noe skrivebeskyttet tekst for spørreskjemaet. Kan brukes til instruksjoner relatert til et felt eller tilleggsinformasjon.

### Bilde
{{< zoomableImage src="/images/questionnaires/questionnaires_13_no.png" caption="Bildekomponent" width="1600" height="600px">}}

Legg til et skrivebeskyttet bilde i spørreskjemaet for å vise instruksjoner eller tilleggsinformasjon relatert til et spørsmål.

### Enkeltvalg
{{< zoomableImage src="/images/questionnaires/questionnaires_14_no.png" caption="Enkeltvalgkomponent" width="1600" height="600px">}}

Opprett en spørsmål/svar-kombinasjon som lar personen som fyller ut et spørreskjema velge en enkelt valgmulighet.

### Flervalg
{{< zoomableImage src="/images/questionnaires/questionnaires_15_no.png" caption="Flervalgskomponent" width="1600" height="600px">}}

Opprett en spørsmål/svar-kombinasjon som lar personen som fyller ut et spørreskjema velge flere alternativer.

### Rangering
{{< zoomableImage src="/images/questionnaires/questionnaires_16_no.png" caption="Rangeringskomponent" width="1600" height="600px">}}

Opprett en spørsmål/svar-kombinasjon som lar personen som fyller ut et spørreskjema rangere alternativene fra øverst til nederst.

### Heltall
{{< zoomableImage src="/images/questionnaires/questionnaires_17_no.png" caption="Heltallskomponent" width="1600" height="600px">}}

Opprett et heltalls inndatafelt for spørreskjemaet ditt (f.eks. alder på en bruker, gateadresse).

### Desimal
{{< zoomableImage src="/images/questionnaires/questionnaires_18_no.png" caption="Desimalkomponent" width="1600" height="600px">}}

Opprett et desimaltall inndatafelt for spørreskjemaet ditt (for eksempel prosent 5,5).

### Valuta
{{< zoomableImage src="/images/questionnaires/questionnaires_19_no.png" caption="Valutakomponent" width="1600" height="600px">}}

Opprett et valutatall inndatafelt for spørreskjemaet ditt (for eksempel kostnad 2 000,20).

### Tall i område
{{< zoomableImage src="/images/questionnaires/questionnaires_20_no.png" caption="Tall i område-komponent" width="1600" height="600px">}}

Opprett en numerisk rekkevidde med et minimum og maksimum og en trinnstørrelse. For eksempel vil en aldersskyveknapp med et minimum på 1 og et maksimum på 120 år der trinnstørrelsen er 5 la deg dra skyveknappen i intervaller på 5 år.

### Enlinjetekstfelt
{{< zoomableImage src="/images/questionnaires/questionnaires_21_no.png" caption="Enlinjetekstfeltkomponent" width="1600" height="600px">}}

En enkelt tekst inndatafelt. For eksempel, for å fange opp en brukers etternavn.

### Flere linjers tekstfelt
{{< zoomableImage src="/images/questionnaires/questionnaires_22_no.png" caption="Flere linjers tekstfeltkomponent" width="1600" height="600px">}}

Et flerlinjet tekst inndatafelt for å fange opp mer informasjon i tekst.

### Risiko
{{< zoomableImage src="/images/questionnaires/questionnaires_23_no.png" caption="Risikokomponent" width="1600" height="600px">}}

Velg en risikomodell kategorigruppe å legge til i spørreskjemaet.

{{< zoomableImage src="/images/questionnaires/questionnaires_24_no.png" caption="Risikomodellvisning" width="1600" height="600px">}}

Lar deg utføre en risikoanalysevurdering i spørreskjemaet.

## Spørreskjema-versjoner

{{< zoomableImage src="/images/questionnaires/questionnaires_5_no.png" caption="Spørreskjema-versjoner" width="1600" height="600px">}}

Hver gang du lagrer spørreskjemaet, lager vi en ny versjon. Når du er klar, kan du klikke på `Utgiver`-knappen for å gjøre den gjeldende versjonen tilgjengelig for å legge til i aktiviteter.

## Forhåndsvisning av spørreskjema

{{< zoomableImage src="/images/questionnaires/questionnaires_6_no.png" caption="Forhåndsvisning av spørreskjema" width="1600" height="600px">}}

Vi kan forhåndsvise spørreskjemaet ved å se hvordan det blir gjengitt ved å klikke på `Forhåndsvisning (øye)`-knappen. Du kan samhandle med elementene, men ikke lagre dem.