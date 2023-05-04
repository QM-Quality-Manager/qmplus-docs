---
title: "Administrator/Bruker"
description: "En brukerveiledning for arbeid med brukere"
lead: "En brukerveiledning for arbeid med brukere. Vi dekker hvordan du oppretter og endrer brukere."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 6
toc: true
---
Denne delen omhandler administrasjon av brukere i systemet.

Ved å klikke på `Administrator/Bruker` får du tilgang til listen over brukere.

## Brukerliste
{{< zoomableImage src="/images/users/user_1.png" caption="Oversikt over brukerliste" width="1600" height="600px">}}

Brukerlisten viser deg alle tilgjengelige brukere i systemet. I denne visningen kan du velge mellom å se de **aktive**, **inaktive** og **alle** brukerne.

Søkefeltet lar deg gjøre et fritekstsøk for å filtrere brukerne du ser etter fornavn, mellomnavn eller etternavn, samt e-post og telefonnummer.

Ved å klikke på filterknappen kan du begrense søket enda mer, som vist nedenfor.

{{< zoomableImage src="/images/users/user_13.png" caption="Filtrer brukere" width="1600" height="600px">}}

Alternativene for filtrering er som følger.

| Filter | Beskrivelse |
| --- | --- |
| `Synlighet` | Vis bare brukere i `Alle avdelinger`, `Denne avdelingen` eller `Bare underavdelinger` |
| `Brukertype` | Vis bare brukere som har en spesifikk brukertype |
| `Tillatelse/Rolle` | Vis alle brukere som har en spesifikk tillatelse/rolle |

Alle disse filtrene kan kombineres for å begrense søket enda mer.

{{< zoomableImage src="/images/users/user_12.png" caption="Ny arbeidsflytdialog" width="1600" height="600px">}}

## Opprett bruker

### Generelle innstillinger

{{< zoomableImage src="/images/users/user_4.png" caption="Ny arbeidsflytdialog" width="1600" height="600px">}}

Dialogen for å opprette brukere lar oss lage nye brukere i systemet og angi brukertypene deres samt egendefinerte tillatelser. Til slutt kan vi justere varslingsinnstillingene.

Følgende er tilgjengelige.

| Felt | Påkrevd | Beskrivelse |
| --- | --- | --- |
| `Brukernavn` | **X** | Påloggingsnavnet for brukeren (må være unikt i systemet) |
| `Passord` | **X** | Brukerens passord |
| `Bekreft passord` | **X** | Bekreft passordet i dette feltet |
| `Fornavn` | **X** | Brukerens fornavn |
| `Mellomnavn` |  | Brukerens mellomnavn |
| `Etternavn` | **X** | Brukerens etternavn |
| `Språk` | **X** | Brukerens foretrukne grensesnittspråk |
| `E-post` | **X** | Brukerens e-post |
| `Telefon` |  | Brukerens telefonnummer |
| `Kommentar` |  | Eventuelle kommentarer om brukeren, for eksempel tilleggsinformasjon om brukeren som er opprettet. |

Når disse feltene er fylt ut, må vi tilordne minst én `avdeling` og `brukertype` kombinasjon. Klikk på fanen `Typer og tillatelser`.

### Avatar

Vi kan endre avataren for brukeren ved å klikke på `avatar`-sirkelen. Alternativene her er å endre bakgrunnsfargen, laste opp et bilde eller ta et bilde med webkameraet.

{{< zoomableImage src="/images/users/user_10.png" caption="Velg farge på avatar eller last opp/webkamera" width="1600" height="600px">}}

Nedenfor kan vi se dialogen der vi kan laste opp et bilde eller bruke webkameraet (krever at brukeren gir tillatelser for å få tilgang til kameraet).

{{< zoomableImage src="/images/users/user_11.png" caption="Last opp bilde eller ta webkamera-bilde" width="1600" height="600px">}}

Når du har lastet opp et bilde eller tatt et bilde med webkameraet, kan du justere opptaksområdet og angi resultatet.

{{< zoomableImage src="/images/users/user_15.png" caption="Juster avatarbilde" width="1600" height="600px">}}

### Avdeling og brukertyper

{{< zoomableImage src="/images/users/user_5.png" caption="Avdelings- og brukertypevisning" width="1600" height="600px">}}

Hver bruker må ha minst én `avdeling` og `brukertype`-kombinasjon lagt til. En bruker kan ha flere kombinasjoner av `avdeling` og `brukertype`, men ingen dupliserte roller.

> For eksempel kan en administrator ha to kombinasjoner.
>
> For toppavdelingen kan de være en `administrator`.
> Samtidig er de en `ansatt` i en annen avdeling.

{{< zoomableImage src="/images/users/user_7.png" caption="Velg avdeling" width="1600" height="600px">}}

{{< zoomableImage src="/images/users/user_8.png" caption="Velg brukertype" width="1600" height="600px">}}

Effekten av å ha flere kombinasjoner av `avdeling` og `brukertype` vil føre til en dialog når du logger inn, slik at du kan velge hvilken kombinasjon
du skal logge inn som.

{{< zoomableImage src="/images/users/user_14.png" caption="Endre avdeling og brukertype" width="1600" height="600px">}}

Du får også tilgang til å endre avdeling/brukertype-kombinasjonen i en rullegardinmeny øverst til høyre. Ved å klikke på en av kombinasjonene, vil visningen din
av applikasjonen endres, og lar deg bytte fra for eksempel en `ansatt`-visning av organisasjonen til en `administrator`-visning.

### Egendefinerte tillatelser/roller

{{< zoomableImage src="/images/users/user_9.png" caption="Egendefinerte tillatelser/roller" width="1600" height="600px">}}

I tillegg til å sette kombinasjoner av `avdeling` og `brukertype`, kan du også legge til brukerspesifikke tillatelser/roller. Dette lar deg kontrollere tillatelsene til en bestemt bruker på en finmasket måte, ved å bruke brukertypen som utgangspunkt.

### Varsler

{{< zoomableImage src="/images/users/user_6.png" caption="Varslingsfanen" width="1600" height="600px">}}

I varslingsfanen kan du angi varslingsinnstillingene for brukeren.

## Brukererstatninger

### Listevisning

{{< zoomableImage src="/images/users/user_2.png" caption="Erstatningsliste" width="1600" height="600px">}}

Fanen `Brukererstatninger` lar oss opprette `erstatninger` for ansatte, slik at vi kan delegere ansvar til andre brukere for en bestemt tidsperiode.

> Erstatninger kan brukes til å delegere ansvar i tilfeller som ferie, sykemelding eller foreldrepermisjon.

Som vi ser fra listen, får vi en komplett oversikt over erstatningene.

Dette lar oss vite hvem som blir erstattet, hvem som erstatter personen, hvilken kombinasjon av `avdeling` og `brukertype` erstatningen gjelder for, og til slutt varigheten av erstatningen.

> Hvis vi bestemmer oss for å slette en erstatningsoppføring, har vi to scenarier.
> 
> 1. Hvis perioden ikke er aktiv, blir hele erstatningen slettet.
> 2. Hvis vi allerede er i erstatningsperioden, blir den avkortet (sluttdatoen endres til gjeldende dato og tid).

### Opprett erstatning

{{< zoomableImage src="/images/users/user_3.png" caption="Ny arbeidsflytdialog" width="1600" height="600px">}}

Vi kan enkelt opprette erstatninger av en bruker med en annen. Først velger du brukeren som skal erstattes. Dette vil deretter vise deg listen over deres `avdeling` og `brukertype`. Velg hvilken kombinasjon du ønsker å erstatte. Velg deretter den `erstattende` brukeren og angi perioden `erstatningen` gjelder. Til slutt klikker du `Lagre` for å opprette erstatningsregelen.

> En `erstattende` bruker vil nå se den ekstra `avdeling` og `brukertype`-kombinasjonen dukke opp i listen over tilgjengelige alternativer ved innlogging.
>
> Data som er rutet til den opprinnelige brukeren, vil nå også bli rutet til `erstatnings`-brukeren i stedet for den opprinnelige brukeren.