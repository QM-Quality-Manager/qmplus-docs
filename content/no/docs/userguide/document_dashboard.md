---
title: "Administrator/Dokument Dashboard"
description: "En brukerveiledning for arbeid med dokumentdashboardene"
lead: "En brukerveiledning for arbeid med dokumentdashboardene. Vi dekker hvordan du oppretter, oppdaterer og administrerer dokumentdashboards."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 10
toc: true
---
Denne delen omhandler håndtering av dokumenter i systemet og organisering av publiseringen for sluttbrukere.

Ved å klikke på `Administrator/Dokument Dashboard` får du tilgang til dokumentbehandleren. Dokumentdashbord lar deg organisere visningen av dokumenter for sluttbrukere ved å velge fra dokumentbiblioteket ditt (som representeres av dokumentbehandleren) og bygge strukturkomponenter eller søkekomponenter for å vise dokumentene.

## Liste over dokumentdashbord

{{< figure src="/images/document_dashboards/document_dashboards_1_no.png" caption="Liste over dashbord" width="1024">}}

Listen over dashbord gir grunnleggende informasjon om hvert dashbord, inkludert tittel, opprettelsesdato, avdelingen som dashbordet er registrert på, synlighet og posisjon i listen over dashbord som brukeren vil se. Fra dette grensesnittet kan du også slette dashbord.

## Opprett et nytt dokumentdashbord

{{< figure src="/images/document_dashboards/document_dashboards_16_no.png" caption="Opprett et nytt dokumentdashbord" width="1024">}}

For å lage et nytt `Dokument Dashboard` må du fylle ut følgende felt:

| Felt | Beskrivelse |
| --- | --- |
| `Tittel på dokumentdashbordet` | Navnet på dashbordtittelen, støtter flere språk. |
| `Synlighet` | Synlighet for dokumentdashbordet. |
| `Avdeling` | Avdelingen hvor dashbordet befinner seg. |
| `Posisjon` | Posisjonen i listen over dashbord som brukeren kan se når de klikker på alternativet `Dokumenter`. |

Etter å ha fylt ut og valgt alternativer, klikk på `Lagre`-knappen for å lage et tomt `Dokument dashboard`, som lar deg bygge komponenter for det.

Når du bygger nye dashbord eller redigerer eksisterende, er det tre faner vi bryr oss om:

| Fane | Beskrivelse |
| --- | --- |
| `Generell` | Generelle innstillinger for `dokument dashboard`. |
| `Komponenter` | En liste over komponenter som er lagt til i dashbordet, inkludert synlighetsinnstillingene deres. Denne listen viser alle dashbordkomponenter uavhengig av synlighets- og avdelingsinnstillingene deres. |
| `Forhåndsvisning` | En forhåndsvisning/bygger for komponenter. Denne komponenten oppdateres når du endrer den valgte avdelingen, slik at du kan se hvordan dashbordet ser ut avhengig av valgt avdeling. |

## Forhåndsvisning

{{< figure src="/images/document_dashboards/document_dashboards_4_no.png" caption="Forhåndsvis dashbordet" width="1024">}}

`Forhåndsvisning`-fanen brukes til å konfigurere utseendet og innholdet i det aktuelle dokumentdashbordet. De tilgjengelige alternativene er:

| Alternativ | Beskrivelse |
| --- | --- |
| `Antall kolonner` | Lar deg spesifisere antall kolonner som vises i dashbordet. |
| `Konfigurer` | Konfigurer dashbordet, inkludert å legge til eksisterende komponenter eller lage nye. |
| `Legg til komponent` | Legg raskt til en ny struktur- eller søkekomponent. |

### Forhåndsvisning > Konfigurer

{{< figure src="/images/document_dashboards/document_dashboards_5_no.png" caption="Konfigurer et dashbord" width="1024">}}

Konfigurer-knappen åpner `Konfigurer`-sidebar, som gir tilgang til å legge til konfigurasjoner fra enten `Generell`-komponentlisten eller brukerens `Mine komponenter`-liste.

> For å legge til komponenter i `Generell`-komponentlisten, må du ha tillatelse til å operere på generelle komponenter. Ellers kan du bare velge eksisterende komponenter fra `Generell`-komponentlisten.

Hver komponent kan legges til ved å skyve vekselen på høyre side til enden, som vil legge til komponenten i gjeldende dashbord.

Hvis listen over komponenter er lang, kan du filtrere dem ved å klikke på søkeikonet og begrense listen ved å søke etter komponentens navn.

Ved å klikke på `Legg til komponent` kan du legge til en ny `Struktur` eller `Liste Søk`-komponent. Se `Legg til komponent`-delen for mer informasjon om å opprette nye komponenter.

### Forhåndsvisning > Legg til komponent

{{< figure src="/images/document_dashboards/document_dashboards_6_no.png" caption="Legg til en komponent i et dashbord" width="1024">}}

Når du klikker på `Legg til komponent`-knappen, kan du velge mellom `Statisk Struktur` og `Liste`-alternativene.

| Alternativ | Beskrivelse |
| --- | --- |
| `Statisk Struktur` | En statisk struktur av dokumenter som lar brukeren bygge strukturen manuelt ved å legge til en katalog- og filstruktur definert av brukeren. |
| `Liste` | En liste over dokumenter basert på et søk, som lar brukeren bruke koder og andre restriksjoner for å gruppere dokumenter. Dette skaper dynamiske visninger som hjelper med å organisere dokumenter automatisk, da nye dokumenter som samsvarer med søket, vil vises automatisk. |

### Forhåndsvisning > Legg til strukturkomponent

{{< figure src="/images/document_dashboards/document_dashboards_10_no.png" caption="Legg til en strukturkomponent i et dashbord" width="1024">}}

Strukturkomponentene lar deg bygge helt egendefinerte katalog- og filkomponenter, og organisere strukturen etter behov. Feltalternativene er:

| Alternativ | Beskrivelse |
| --- | --- |
| `Komponentnavn` | Navnet på dashbordkomponenten. |
| `Farge` | Fargen på dashbordkomponenten. |
| `Type` | Typen av komponenten, som lar deg bytte mellom strukturkomponent og liste. |
| `Synlighet` | Synligheten til komponenten. |
| `Avdeling` | Avdelingen til komponenten. |
| `Statisk struktur > Ny mappe` | Legg til en ny mappe i strukturen. |
| `Statisk struktur > Legg til dokument` | Legg til et nytt dokument i strukturen. |

Ved å klikke på `Legg til dokument`-ikonet åpnes en sidebar, som lar deg bla gjennom dokumentbehandlerfiler og legge til dokumenter.

{{< figure src="/images/document_dashboards/document_dashboards_11_no.png" caption="Bla etter dokumenter" width="1024">}}

Du kan bla gjennom dokumentmappene, filtrere og søke etter filer, og deretter velge flere filer for å legge til på en gang. Når du er klar, klikker du på `Velg N dokumenter`-knappen for å legge dem til `Struktur`-komponenten din.

Ved å klikke på `Legg til mappe`-ikonet åpnes en sidebar som lar deg lage en ny dokumentmappe og legge den til i `Struktur`-komponenten din.

{{< figure src="/images/document_dashboards/document_dashboards_12_no.png" caption="Legg til en mappe i strukturkomponenten" width="1024">}}

Skriv inn navnet på mappen (støtter flere språk) og klikk på `Lagre endringer`-knappen for å legge til mappen i strukturen din.

{{< figure src="/images/document_dashboards/document_dashboards_13_no.png" caption="Eksempel på strukturkomponent" width="1024">}}

Ovenfor er et bilde av en `Struktur`-komponent som inneholder en `Filmappe` og et par `Dokumenter`. Du kan endre rekkefølgen på elementene ved å dra dem. For å flytte et dokument under en `Filmappe`, drar du det fra venstre til høyre under en mappe, og det vil bli festet under den `Filmappen`. Dokumenter og mapper kan også fjernes fra strukturkomponenten.

### Forhåndsvisning > Legg til liste komponent

{{< figure src="/images/document_dashboards/document_dashboards_8_no.png" caption="Legg til en liste komponent" width="1024">}}

En liste komponent er en komponent som kjører et `Søk` etter dokumenter og viser eventuelle matchende dokumenter. Alternativene for komponenten er:

| Alternativ | Beskrivelse |
| --- | --- |
| `Sortering` | Definerer sorteringsrekkefølgen for dokumentene i listen. |
| `Filtre` | Legg til filtre for å begrense dokumentene som vises i listen. |

For å sortere listen er det følgende alternativer:

| Sorteringsalternativ | Beskrivelse |
| --- | --- |
| `Registrert den` | Sorter etter dokumentets `Registrert den`-dato. |
| `Endret den` | Sorter etter dokumentets `Endret den`-dato. |
| `Type` | Sorter etter dokumenttypen. |
| `Navn` | Sorter etter dokumentnavnet. |

Sorteringsrekkefølgen kan være i `Synkende` eller `Stigende` rekkefølge.

For å filtrere listen er det følgende alternativer:

| Filteralternativ | Beskrivelse |
| --- | --- |
| `Periode` | Perioden for dokumentet etter enten `Registrert den` eller `Endret den`. |
| `Søk` | Et tekstsøk på navnet til dokumentene. |
| `Etiketter` | Et sett med etiketter adskilt med komma. |
| `Saksstatus` | Dokumenter med en spesifikk saksstatus. |
| `Dokumentmappe` | Filtrer etter en bestemt dokumentmappe i dokumentbehandleren. |

### Forhåndsvis resultat

{{< figure src="/images/document_dashboards/document_dashboards_14_no.png" caption="Forhåndsvisning av dashbord med struktur- og listekomponent" width="1024">}}

Ovenfor er et eksempel på et `Dashboard` med en `Liste` og `Struktur`-komponent. Som vi kan se, kan vi `Minimer/Maksimer` komponenten, samt endre størrelse og flytte komponenten på dashbordet. Eksisterende komponenter kan også rekonfigureres og fjernes fra `Dashbordet`.