---
title: "Administrator/Dokument Administrator"
description: "En brukerveiledning for å jobbe med dokumentadministratoren"
lead: "En brukerveiledning for å jobbe med dokumentadministratoren. Vi dekker hvordan du oppretter, oppdaterer og administrerer dokumenter."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 9
toc: true
---
Denne seksjonen er dedikert til å håndtere dokumenter i systemet.

Ved å klikke på `Administrator/Dokument Administrator`, får du tilgang til dokumentbehandleren.

## Dokumentbehandler

{{< zoomableImage src="/images/document_manager/document_manager_1_no.png" caption="Dokument administrator" width="1600" height="600px">}}

Dokumentbehandleren er det sentrale knutepunktet for dokumenthåndteringssystemet. Den lar deg organisere dokumenter, opprette nye, laste opp eksisterende, redigere dem eller deaktivere dem.

{{< zoomableImage src="/images/document_manager/document_manager_3_no.png" caption="Filtrering av dokumenter" width="1600" height="600px">}}

Ved å bruke filteret kan du avgrense dokumentene som vises i dokumentbehandleren for å fokusere på et bestemt dokument.

> Husk at alle dokumenter er knyttet til avdelinger. Dette betyr at visningen av dokumenter i behandleren vil endre seg når du endrer synligheten og avdelingen du ser på. For eksempel, for å se alle dokumenter i underavdelingene, kan du velge `Alle` fra `Synlighet for dokumentmapper`.

## Opprett en ny mappe

{{< zoomableImage src="/images/document_manager/document_manager_4_no.png" caption="Lag en ny mappe" width="1600" height="600px">}}

For å opprette en ny mappe, oppgi mappenavnet på flere språk, hvis det støttes.

## Dokumentmappesvisning

{{< zoomableImage src="/images/document_manager/document_manager_5_no.png" caption="Dokumentmappevisning" width="1600" height="600px">}}

Når du velger en dokumentmappesvisning, har du følgende alternativer tilgjengelig:

| Alternativ | Beskrivelse |
| --- | --- |
| `Ny mappe` | Opprett en ny mappe under det valgte dokumentet på venstre side. |
| `Nytt dokument` | Opprett et nytt dokument i denne dokumentmappen. |
| `Oppdater` | Oppdater gjeldende dokumentmappesvisning. |
| `Gi nytt navn` | Gi nytt navn til gjeldende dokumentmappe. |
| `Last opp` | Last opp et dokument i denne dokumentmappen. |

> Du kan også laste opp dokumenter ved å dra og slippe dem direkte i dokumentmappen.

{{< zoomableImage src="/images/document_manager/document_manager_18_no.png" caption="Opplastingsskjema etter å ha droppet fil på dokumentmappen" width="1600" height="600px">}}

Når en eller flere filer slippes på dokumentmappen, dukker det opp en opplastingsdialog med følgende alternativer:

| Alternativer | Beskrivelse |
| --- | --- |
| `Filer` | Listen over dokumenter som blir lastet opp når du klikker på `Last opp`-knappen. |
| `Synlighet` | Angi synligheten til de opplastede dokumentene. |
| `Arbeidsflyt` | Velg arbeidsflyten som alle de opplastede dokumentene vil bli knyttet til. |

> Du kan også bruke `Last opp`-knappen for å laste opp filer i stedet for å dra og slippe filer.

## Opprett et nytt dokument

{{< zoomableImage src="/images/document_manager/document_manager_19_no.png" caption="Opprett dokumentvisning" width="1600" height="600px">}}

Når du klikker på `Nytt dokument`-knappen, vises dialogen for nytt dokument med følgende alternativer:

| Alternativ | Beskrivelse |
| --- | --- |
| `Dokumenttittel` | Tittelen på det nye dokumentet, støtter flere språk. |
| `Dokumentposisjon` | Listen over dokumentposisjoner (synlighet og avdeling) knyttet til det nye dokumentet. |
| `Dokumenttype` | Typen dokument, se tabellen nedenfor. |
| `Arbeidsflyt` | Velg den tilknyttede arbeidsflyten for det nye dokumentet du oppretter. |
| `Tilgjengelige dokumentmaler` | Valgfritt velg en mal for å basere det nye dokumentet på. |
| `Beskrivelse` | Valgfri beskrivelse for det nye dokumentet. |
| `Tildelte tillatelser` | Tildel tillatelser for å begrense tilgangen til dokumentet. |
| `Merker` | Legg til merker for å gruppere dokumentet med andre dokumenter ved hjelp av nøkkelord. |

De støttede dokumenttypene er som følger:

| Dokumenttype | Beskrivelse |
| --- | --- |
| `Lenke` | Et dokument som representerer en ekstern lenke fra plattformen. |
| `Fil` | En opplastet fil som et Word-dokument, PDF, bilde eller video. |
| `Tekstdokument` | Et enkelt HTML-tekstdokument (med grunnleggende formatering) lagret i systemet. |
| `Prosesskart` | Et prosessdiagram (ligner på et forenklet Visio) for å tegne prosesskart for bruk i applikasjonen. |
| `Richtext` | Et rikt tekstbehandlingsdokument (ligner på et forenklet Microsoft Word) som gir mer kompleks dokumentinntasting.|
| `Regneark` | Et grunnleggende regnearkdokument, med et minimumssett av funksjonalitet. |

### Opprett et nytt `Fildokument`

{{< zoomableImage src="/images/document_manager/document_manager_20_no.png" caption="Opprett et nytt fildokument" width="1600" height="600px">}}

De viktigste aspektene unike for dokumenttilfellet inkluderer:

| Fane | Beskrivelse |
| --- | --- |
| `Dokumentdata` | Inneholder dokumentets plassering og lar deg legge til ytterligere datadeler hvis mer informasjon må registreres for dokumenttilfellet. |
| `Tittel og beskrivelse` | Tittel og beskrivelse av dokumenttilfellet. |
| `Lagrede filer` | Filer lagret for dette dokumenttilfellet. |
| `Versjoner` | Alle versjonene av dette dokumenttilfellet. |

{{< zoomableImage src="/images/document_manager/document_manager_21_no.png" caption="Tittel og beskrivelse-fanen" width="1600" height="600px">}}

På fanen `Tittel og beskrivelse` kan du endre `tittelen`, `beskrivelsen` for alle språk. Du kan også laste opp nye versjoner av filen eller nye filer for forskjellige språk.

> Alle dokumenter på plattformen støtter flere språk, noe som gjør at du kan beholde alle språkversjoner av en prosedyre samlet i ett håndterlig tilfelle. For eksempel kan du ha en produksjonsprosess som må være tilgjengelig på både norsk og engelsk.

### Opprett et nytt **Tekstdokument**

{{< zoomableImage src="/images/document_manager/document_manager_24_no.png" caption="Opprette et nytt tekstdokument" width="1600" height="600px">}}

`Tekstdokumentet` har en `Innhold`-fane som lar deg redigere dokumentet.

{{< zoomableImage src="/images/document_manager/document_manager_23_no.png" caption="Rediger tekstinnhold" width="1600" height="600px">}}

Innholdsredigereren lar deg redigere HTML-lignende innhold med et grunnleggende sett med formateringsalternativer.

### Opprett et nytt **Lenkedokument**

{{< zoomableImage src="/images/document_manager/document_manager_25_no.png" caption="Opprette et nytt lenkedokument" width="1600" height="600px">}}

Det unike området for et `Lenke`-dokument er under fanen `Tittel og beskrivelse`, der du kan angi den eksterne lenken som er knyttet til dette dokumentet.

> Det er mulig å oppgi flere lenker i samme dokumenttilfelle, én for hvert språk.

### Opprett et nytt **Prosesskartdokument**

{{< zoomableImage src="/images/document_manager/document_manager_32_no.png" caption="Opprette et nytt prosessdokument" width="1600" height="600px">}}

Prosesskartverktøyet lar deg lage enkle prosesskart som du kan lagre som dokumenter, bygge inn i dashbord eller lenke til andre dokumenter, og lage klikkbare kart.

### Opprett et nytt **Richtext-dokument**

{{< zoomableImage src="/images/document_manager/document_manager_33_no.png" caption="Opprett et nytt Rik tekst-dokument" width="1600" height="600px">}}

Et mer Microsoft Word-lignende grensesnitt for rikere dokumenter.

### Opprett et nytt **Regnearkdokument**

Et grunnleggende Excel-lignende grensesnitt for mer sofistikerte regneark.

{{< zoomableImage src="/images/document_manager/document_manager_34_no.png" caption="Opprett et nytt regneark" width="1600" height="600px">}}

## Redigere et eksisterende dokument

{{< zoomableImage src="/images/document_manager/document_manager_42_no.png" caption="Redigere et eksisterende dokument" width="1600" height="600px">}}

Når du arbeider med dokumenter, er det viktig å forstå at det er to hovedtilstander dokumenter eksisterer i:

| Tilstand | Beskrivelse |
| --- | --- |
| `Utkast` | Mens du jobber med et dokument og gjør endringer, vil du ved å klikke på `Lagre`-knappen lagre en utkastversjon som ikke er synlig for sluttbrukere. For å gjøre endringene synlige, må du eksplisitt publisere dokumentet. |
| `Publisert` | Et publisert dokument er synlig for sluttbrukere. Dette lar deg gjøre endringer i et dokument privat og bare publisere når du er klar. |

Et dokument kan også merkes som en `Mal`, noe som gjør at du kan bruke det som grunnlag for et nytt dokument. Når du oppretter et nytt dokument fra en `Mal`, vil det bli opprettet fra den nyeste `Publiserte` versjonen.

> For å lage en ny versjon, klikk på knappen `Ny versjon`. Denne knappen er bare aktivert når det gjeldende dokumentet er i en `lukket` tilstand, og det vil tilbakestille arbeidsflyten til begynnelsen, slik at du kan starte en annen versjon av dokumentet.

## Kopier dokument til en annen mappe

{{< zoomableImage src="/images/document_manager/document_manager_6_no.png" caption="Kopier dokumentet til en annen katalog" width="1600" height="600px">}}

Velg et dokument. Når et dokument er valgt, endres verktøylinjen, slik at du kan klikke på `Kopier til`-knappen.

{{< zoomableImage src="/images/document_manager/document_manager_7_no.png" caption="Velg målkatalog" width="1600" height="600px">}}

Velg en målmappe og klikk på `Velg`-knappen for å lage en kopi av dokumentet i en annen mappe.

## Flytt dokument til en annen mappe

{{< zoomableImage src="/images/document_manager/document_manager_8_no.png" caption="Flytt dokumentet til en annen katalog" width="1600" height="600px">}}

For å flytte et dokument til en ny mappe, klikk på `Send til`-knappen og velg deretter en destinasjonsmappe for filen.

## Importer dokumenter fra SharePoint

{{< zoomableImage src="/images/document_manager/document_manager_10_no.png" caption="Sharepoint import" width="1600" height="600px">}}

Hvis `SharePoint` er aktivert som et integrasjonspunkt for organisasjonen din, vil du ha tilgang til en `Importer`-knapp som lar deg importere dokumenter fra konfigurerte `SharePoint`-delinger.

{{< zoomableImage src="/images/document_manager/document_manager_36_no.png" caption="Sharepoint import dialog" width="1600" height="600px">}}

Når du importerer dokumenter fra `SharePoint`, må du fylle inn flere felter som beskrevet nedenfor:

| Felt | Beskrivelse |
| --- | --- |
| `Nettsted` | Velg `SharePoint`-nettstedet (deling) for å importere dokumenter fra. |
| `Dokumenter` | Åpner dokumentnavigatoren, som lar deg velge `SharePoint`-dokumentene du vil importere. |
| `Importer til` | Angi synlighet, avdeling og dokumentmappe for alle importerte dokumenter. |
| `Arbeidsflyt` | Angi den tilknyttede dokumentarbeidsflyten som skal brukes med alle importerte dokumenter. |
| `Synkroniser oppdateringer` | Angi om plattformen vil forespørre `SharePoint` med jevne mellomrom for å sjekke om det finnes nye versjoner av dokumentene og importere de oppdaterte dokumentene automatisk. |

Å klikke på `Dokument`-knappen vil åpne en filbehandler, som lar deg velge dokumenter fra det angitte `SharePoint`-nettstedet.

{{< zoomableImage src="/images/document_manager/document_manager_37_no.png" caption="Valgte filer å importere" width="1600" height="600px">}}

Når du har valgt filene du ønsker å importere, klikk på `Bekreft`-knappen for å gå tilbake til `Importer fra SharePoint`-dialogen.

{{< zoomableImage src="/images/document_manager/document_manager_38_no.png" caption="Importer valgte filer" width="1600" height="600px">}}

For å fullføre importprosessen, klikk på `Importer`-knappen.

{{< zoomableImage src="/images/document_manager/document_manager_31_no.png" caption="Visning av importerte filer" width="1600" height="600px">}}

Som du kan se, har de importerte filene fra `SharePoint` et `SharePoint-logo` og et symbol som indikerer at de ble importert fra `SharePoint`.

## Eksporter dokumenter til SharePoint

{{< zoomableImage src="/images/document_manager/document_manager_39_no.png" caption="Eksporterer filer til Sharepoint" width="1600" height="600px">}}

Velg en eller flere filer, og hvis organisasjonen din har `SharePoint` aktivert, vil brukerne se en `Eksporter`-knapp som lar dem eksportere de valgte dokumentene til `SharePoint`.

{{< zoomableImage src="/images/document_manager/document_manager_40_no.png" caption="Eksport fildialog" width="1600" height="600px">}}

Når du eksporterer dokumenter til `SharePoint`, må du fylle inn flere felter som beskrevet nedenfor:

| Felt | Beskrivelse |
| --- | --- |
| `Nettsted` | Velg `SharePoint`-nettstedet (deling) å eksportere dokumenter til. |
| `Dokumenter` | Listen over dokumenter som eksporteres til SharePoint. |
| `Dokumentmappe` | Mål-mappen i SharePoint for de eksporterte dokumentene. |
| `Synkroniser oppdateringer` | Når avkrysset, vil plattformen automatisk oppdatere dokumentene til SharePoint og holde dem synkroniserte. |

Til slutt, klikk på `Eksporter`-knappen for å fullføre eksporten av dokumenter til `SharePoint`.

{{< zoomableImage src="/images/document_manager/document_manager_41_no.png" caption="Visning av eksporterte filer" width="1600" height="600px">}}

Når du har eksportert dokumentene, vil de være synlige i dokumentbehandleren med et `SharePoint`-symbol og et `Eksport`-symbol.
