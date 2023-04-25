---
title: "Administrator/Preferanser"
description: "En brukerveiledning for arbeid med preferanser"
lead: "En brukerveiledning for arbeid med preferanser. Vi dekker hvordan du oppretter og endrer preferanser."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 21
toc: true
---
Denne delen omhandler administrasjon av innstillinger i systemet.

Ved å klikke på `Administrator/Innstillinger` får du tilgang til listen over innstillinger.

## Generelle innstillinger

{{< figure src="/images/preferences/preferences_1_no.png" caption="Generelle innstillinger" width="1024">}}

De generelle innstillingene lar deg kontrollere følgende egenskaper.

| Egenskap | Beskrivelse |
| --- | --- |
| `Innloggingstittel` | Tittelen som vises når brukeren blir bedt om å taste inn brukernavn og passord. |
| `E-postsending for leietaker` | Aktiver eller deaktiver e-postsending for alle leietakerbrukere. | 

## Saksrelaterte innstillinger

{{< figure src="/images/preferences/preferences_2_no.png" caption="Saksrelaterte innstillinger" width="1024">}}

Disse preferansene kontrollerer grunnleggende forfallsdatoer og varslingsinnstillinger. Disse innstillingene kan overstyres på arbeidsflyt- og skjemanivå.

| Egenskap | Beskrivelse |
| --- | --- |
| `Standard antall dager` | Antall dager fra en sak er registrert til den blir merket som forfalt. |
| `Send et varsel` | Standardinnstillingen for når varsler sendes. |

## E-post

{{< figure src="/images/preferences/preferences_4_no.png" caption="E-postinnstillinger" width="1024">}}

Denne delen lar deg overstyre plattformens e-postinnstillinger. Dette lar brukeren bruke sitt eget SMTP-endepunkt for å sende e-post fra Q. Dette kan være nyttig hvis kunden ønsker at varslene skal komme fra sitt eget e-postdomene eller hvis e-postinnstillingene deres forhindrer vanlig e-post fra Q i å bli levert.

For å aktivere en tilpasset e-postserver, vipp bryteren `Bruk tilpasset SMTP`.

For å konfigurere en e-postserver må du fylle ut følgende felt.

| Felt | Beskrivelse |
| --- | --- |
| `Vert` | SMTP-serverens vert. |
| `Port` | SMTP-serverens port som brukes. |
| `Start TLS` | Hvis serveren bruker SSL for å kryptere tilkoblingen. **VI ANBEFALER STERKT AT TLS AKTIVERES PÅ SERVEREN DIN** |
| `Passord` | Passordet til SMTP-brukeren som brukes for å koble til den utgående e-postserveren. |
| `Brukernavn` | Brukernavnet til SMTP-brukeren som brukes for å koble til den utgående e-postserveren. |
| `Andre SMTP-egenskaper` | Ytterligere plattformspesifikke egenskaper som kreves for å koble til og sende e-post. Kontakt Q hvis disse er nødvendige. |
| `Fra navn` | Hvilket navn eller tekst som skal settes som avsender når du sender e-post. |
| `Fra e-post` | Hvilken e-post som skal angis som avsender. |

På høyre side er det et enkelt send e-post skjema som lar deg teste utsending av e-post via din nylig konfigurerte tilpassede SMTP-server.

> Denne e-posten er kun for utsending og kan ikke brukes til å svare til Q.

## Varsler

{{< figure src="/images/preferences/preferences_5_no.png" caption="Varslingsinnstillinger" width="1024">}}

Varslingsinnstillingene lar deg angi standard varslingsinnstillinger for systemet som helhet.

Du kan bestemme hvilke varsler som skal være brukerjusterbare og hvilke varsler som må sendes ut. Du kan også angi påminnelsesinnstillingene og når de skal sende e-postene. For eksempel kan du sette lavprioritetspåminnelser til å bli sendt hver onsdag, men høyprioritetspåminnelser må sendes hver dag.

Når du velger `Generell regel`, kontrollerer du påminnelsesinnstillingen for hvert prioritetsnivå ved å endre rullegardinmenyen rett under `Generell regel`-innstillingen, og dette vil sette påminnelsesutsendingstiden til å være den samme for alle tilgjengelige prioriteringer.

Hvis du ønsker å angi forskjellige påminnelserstider per prioritet, velg `Spesifikk for hvert prioritetsnivå` i stedet og endre det per prioritet.

> Hvis du setter e-post til `Aktivert`, vil e-post alltid bli sendt. Hvis du setter den til `Brukermodifiserbar`, vil brukerne selv kunne overstyre om de ønsker å motta e-poster eller ikke.

## Sikkerhetsinnstillinger

{{< figure src="/images/preferences/preferences_6_no.png" caption="Sikkerhetsinnstillinger" width="1024">}}

Sikkerhetsinnstillinger lar deg konfigurere følgende alternativer.

| Alternativ | Beskrivelse |
| --- | --- |
| `Streng passordendring` | Aktiver eller deaktiver streng kontroll av passord når du oppretter en ny bruker eller oppdaterer en eksisterende bruker. |
| `Økt tidsavbruddsvarighet i sekunder` | Mengden tid i sekunder en bruker kan være inaktiv før de blir logget ut av systemet. |

## Mobile innstillinger

{{< figure src="/images/preferences/preferences_7_no.png" caption="Mobile innstillinger" width="1024">}}

Mobile innstillinger lar deg konfigurere applikasjonsnivå delte innstillinger for alle mobile klientbrukere.

| Alternativ | Beskrivelse |
| --- | --- |
| `Mobil GPS-lokasjonsopptakspolicy` | Lar deg angi om GPS-lokasjonsopptak skal være tilgjengelig eller ikke. For detaljer om alternativene, se nedenfor. |

## Mobile GPS-lokasjonsopptakspolicy alternativer

| Alternativ | Beskrivelse |
| --- | --- |
| `Alltid ta opp` | Ta alltid opp GPS-koordinater. Brukeren kan ikke deaktivere det. |
| `Never Record` | Aldri ta opp GPS-koordinater. Brukeren kan ikke aktivere det. |
| `User choice, default record` | Ta opp GPS-koordinater som standard. Brukeren **KAN** deaktivere det. |
| `User choice, default no recording` | Ikke ta opp GPS-koordinater som standard. Brukeren **KAN** aktivere det. |

## Innstillinger for opplasting av logoer

{{< figure src="/images/preferences/preferences_8_no.png" caption="Innstillinger for opplasting av logoer" width="1024">}}

Innstillingene for opplasting av logoer lar deg laste opp egendefinerte logoer som skal vises på forskjellige steder.

| Valg | Beskrivelse |
| --- | --- |
| `Firmalogo for dokumenter og innloggingsprompt` | Logo som vises når brukeren får innloggingsprompten. |
| `Liten logo i nettleserens topp venstre hjørne` | Logoen øverst til venstre når du er logget inn. |

## Statusoversikt

{{< figure src="/images/preferences/preferences_9_no.png" caption="Statusoversikt" width="1024">}}

Viser applikasjonsstatistikker. Følgende statistikker er tilgjengelige.

| Valg | Beskrivelse |
| --- | --- |
| `Totalt lagringsplass brukt av filer` | Total lagringsplass brukt av opplastede filer. Dette inkluderer dokumenter så vel som vedlegg til meldinger og saker. |
| `Totalt antall lagrede filer` | Antall lagrede filer. Dette inkluderer dokumenter så vel som vedlegg til meldinger og saker. |

## Integrasjoner

{{< figure src="/images/preferences/preferences_10_no.png" caption="Innstillinger for integrasjoner" width="1024">}}

Viser alle tilgjengelige integrasjonsalternativer for abonnementet ditt.

> Noen integrasjoner må aktiveres spesifikt for abonnementet ditt (kostnader kan påløpe). Hvis du er interessert i spesifikke Enterprise-integrasjoner, ta kontakt med oss.

| Integrasjon | Enterprise-alternativ | Beskrivelse |
| --- | --- | --- |
| `LDAP` | **JA** | Synkroniser brukere og avdelinger mot en LDAP-server. |
| `OAuth` | **JA** | Tillat enkelt pålogging-integrasjon med en OAuth 2.x-leverandør. |
| `Markedsplass` | | Aktiver tilgang til Q Marketplace. |
| `MS Teams` | **JA** | Integrer med Microsoft Teams. Krever OAuth-integrasjon mot Azure med riktig oppsett av tillatelser. |
| `SharePoint` | **JA** | Integrer med SharePoint. Krever OAuth-integrasjon mot Azure med riktig oppsett av tillatelser. |
| `Kalender` | **JA** | Integrer med kalender. Krever OAuth-integrasjon mot Azure med riktig oppsett av tillatelser. |
