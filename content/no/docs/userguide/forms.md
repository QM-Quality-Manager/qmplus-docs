---
title: "Administrator/Skjemaer"
description: "En brukerveiledning for arbeid med skjemaer"
lead: "En brukerveiledning for arbeid med skjemaer. Vi dekker hvordan du oppretter og endrer skjemaer."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 13
toc: true
---
Denne seksjonen handler om å håndtere skjemaer i systemet. Få tilgang til listen over skjemaer ved å klikke på `Administrator/Skjemaer`.

## Skjemaliste

{{< figure src="/images/forms/forms_1_no.png" caption="Liste over alle gjeldende skjemaer" width="1024">}}

Skjemalisten viser alle skjemaer registrert i systemet. Du kan filtrere etter `Aktive`, `Inaktive` og `Alle` skjemaer, samt søke etter tekst. For flere filtreringsalternativer, klikk på bruk filter-knappen for å få tilgang til sidepanelet.

{{< figure src="/images/forms/forms_9_no.png" caption="Filtrere skjemaliste" width="1024">}}

Følgende filtre er tilgjengelige for skjemalistingen:

| Filter | Beskrivelse |
| --- | --- |
| `Synlighet` | Filtrer etter skjemaets synlighetstype (`Avdeling`, `Avdeling og underavdelinger` osv.) |
| `Skjematype` | Filtrer skjemaene etter skjematype. |

## Opprette et nytt skjema

{{< figure src="/images/forms/forms_2_no.png" caption="Opprette et nytt skjema" width="1024">}}

For å opprette et nytt skjema, oppgi følgende informasjon:

| Felt | Påkrevd | Beskrivelse |
| --- | --- | --- |
| `Skjemnavn` | **X** | Skjemats tittel, støtter flere språk. |
| `Skjematype` | **X** | Velg en av `Skjematyper` fra systemet. |
| `Anonymitet` | **X** | Velg om skjemaet støtter anonym registrering av data. |
| `Synlighet` | **X** | Angi synligheten for skjemaet. |
| `Avdeling` | **X** | Angi avdelingen der skjemaet er synlig. |
| `Enhetsplattformsynlighet` | | Tillat valg av plattformene skjemaet er tilgjengelig på (Web, Mobil, Alle); ingen valg betyr Alle som standard. |
| `Oppgavemaler` | | Velg en valgfri `Oppgavemal` som vil opprette et sett med oppgaver i en sak når en ny skjemaregistrering skjer. |
| `Beskrivelse` | | En lang tekstbeskrivelse for skjemaet, støtter flere språk. |
| `Knapptekst` | | Teksten som vises i registrer skjema-menyen, støtter flere språk. |
| `Referanser` | | Legg til dokumentreferanser til skjemaet fra dokumentbiblioteket ditt. |
| `Rettigheter` | | Begrens skjemaet basert på system- eller tilpassede tillatelser. |

Etter å ha angitt de nødvendige feltene og eventuell tilleggsinformasjon, kan du opprette skjemaet og gjøre det tilgjengelig for bruk i systemet.

DONE
----------------------------------------------------------------------------------------------------------
## Bygge et skjema

{{< figure src="/images/forms/forms_4_no.png" caption="Bygge et skjema" width="1024">}}

`Layout-fanen` lar deg begynne å bygge `Skjemaet` ved hjelp av ulike komponenter. Klikk på `Opprett nytt element` for å få tilgang til en popup-meny med tilgjengelige komponenter.

{{< figure src="/images/forms/forms_7_no.png" caption="Tilgjengelige komponenter" width="1024">}}

Komponentene du kan legge til i skjemaet er:

| Komponent | Beskrivelse |
| --- | --- |
| `Registrert av` | Viser personen som registrerte skjemainngangen. |
| `Dato/Tid` | Legg til et felt for å registrere en dato- og tidkombinasjon. |
| `Registrert på vegne av` | Lar personen som fyller ut skjemaet angi hvem de registrerer inngangen på vegne av. |
| `Registrert på avdeling` | På hvilken avdeling skal skjemainngangen registreres. |
| `Velg saksbehandler` | Lar personen som fyller ut skjemaet velge en saksbehandler direkte, slik at det blir sendt til en person å jobbe med. |
| `Beskriv omstendighetene/avviket her` | Tekstbeskrivelse brukt til å beskrive omstendighetene eller avviket. |
| `Feilkostnad til nå` | Den estimerte kostnaden i pengeverdi til nå. |
| `Prioritet` | Lar brukeren angi en prioritet for skjemainngangen. |
|||
| `Definerende kategorigruppe` | Legger til en definerende kategorigruppe i skjemaet. |
| `Kategorigruppe` | Legger til en normal kategorigruppe i skjemaet. |
| `Etikett` | En tekstetikett for å legge til struktur i skjemaet. |
|||
| `Fil` | En filopplastingskomponent som lar sluttbrukeren laste opp en fil. |
| `Bilde` | Legg til et bilde i skjemaet. For eksempel en instruksjonsdiagram. |
| `Manuell signatur` | Et felt som aksepterer manuelle signaturer. |
|||
| `Tekstfelt` | Et en-linjers tekstfelt. |
| `Rik tekstredigeringsfelt` | Et rik tekstredigeringsfelt. |

Et skjema kan ha en enkelt, dobbel eller tredobbelt kolonneoppsett.

> For mobil-only skjemaer anbefaler vi en enkelt kolonne, men mobilklienten støtter også endring av kolonner.

### Konfigurere en kategorikomponent

{{< figure src="/images/forms/forms_8_no.png" caption="Konfigurere en kategorikomponent" width="1024">}}

En kategorigruppe tilbyr flere konfigurasjonsalternativer:

| Alternativer | Beskrivelse |
| --- | --- |
| `Render-type` | Hvordan kategorigruppen skal gjengis. |
| `Obligatorisk` | Er kategorigruppen obligatorisk. |
| `Kun synlig ved saks-overflow` | Kun synlig for saksbehandlere. Ikke synlig for personen som fyller ut et skjema. |
| `Synlig på mobil` | Er synlig på mobil. |
|||
| `Overstyr synlighet` | Overstyr skjemaets synlighet for denne kategorigruppen alene. For eksempel hvis du vil vise en kategorigruppe kun for en underavdeling. |
| `Synlighet` | Angi overstyrt synlighet. |
| `Avdeling` | Angi overstyrt avdeling. |
|||
| `Kategorigruppe` | Kategorigruppen lar designeren velge et utvalg av kategorier å vise i skjemaet. |

Tilpass skjemaet ved å legge til og konfigurere komponenter for å dekke dine behov, og sørg for at det fanger all nødvendig informasjon for din spesifikke brukssak.

De tilgjengelige render-typene for kategorikomponenter er:

| Alternativer | Beskrivelse |
| --- | --- |
| `Auto` | Velger automatisk den mest passende komponenten avhengig av antall kategorier. Hvis det er mange kategorier, vil den bytte til en rullegardinmeny. |
| `Rullegardin` | En rullegardinmeny med kategorier. |
| `Radioknapper` | Radioknapper for `enkeltvalg`-kategorier. |
| `Avkrysningsbokser` | Avkrysningsbokser for `flervalg`-kategorigrupper. |

### Konfigurering av et tekstelement

{{< figure src="/images/forms/forms_12_no.png" caption="Konfigurering av et tekstelement" width="1024">}}

Et tekstelement har flere konfigurasjonsalternativer:

| Alternativer | Beskrivelse |
| --- | --- |
| `Obligatorisk` | Bestemmer om kategorigruppen er obligatorisk. |
| `Kun synlig ved saks-overflow` | Kun synlig for saksbehandlere, ikke synlig for personen som fyller ut et skjema. |
| `Synlig på mobil` | Indikerer om elementet er synlig på mobile enheter. |
| `Støtte for strekkodelesing` | Aktiverer støtte for strekkode-skanning for feltet. |
| `Maks lengde` | Angir maksimal lengde på tekstfeltet. |
|||
| `Overstyr synlighet` | Overstyrer skjemaets synlighet for denne kategorigruppen alene, nyttig hvis du vil vise en kategorigruppe kun for en underavdeling. |
| `Synlighet` | Angir overstyrt synlighet. |
| `Avdeling` | Angir overstyrt avdeling. |

## Forhåndsvisning av skjema

{{< figure src="/images/forms/forms_5_no.png" caption="Forhåndsvisning av skjema" width="1024">}}

Funksjonen for forhåndsvisning av skjema lar deg teste hvordan skjemaet oppfører seg.

| Modus | Beskrivelse |
| --- | --- |
| `Under registrering` | Viser skjemaet slik det vises for brukeren som fyller ut skjemaet. |
| `Under saksbehandling` | Viser skjemaet slik det vises for en saksbehandler etter å ha åpnet den registrerte skjemaoppføringen. |

> For å se hvordan skjemaet vil bli gjengitt i forskjellige avdelinger, klikk på avdelingen øverst til høyre og endre avdelingen.

{{< figure src="/images/forms/forms_6_no.png" caption="Endre avdelingsvisning" width="1024">}}

## Behandlingsinnstillinger

Behandlingsfanen inneholder innstillinger for å angi standard saksfrister og eskaleringer for dette bestemte skjemaet. Hvis de er angitt, vil disse innstillingene overstyre eventuelle spesifikasjoner på arbeidsflytnivå.

{{< figure src="/images/forms/forms_3_no.png" caption="Behandlingsinnstillinger" width="1024">}}

### Forfallsdatoer

Denne funksjonen lar deg styre hvordan forfallsdato varsler håndteres. Det lar deg angi generelle innstillinger for håndtering av forfallsdatoer for en arbeidsflyt, som vil gjelde for alle `skjemaer` som bruker den arbeidsflyten.

> `Skjemaer` lar deg overstyre disse innstillingene. For eksempel kan du ha et `Ulykkes`-skjema med mye kortere automatiske forfallsdatoer sammenlignet med den generelle arbeidsflyten. `Skjema`-innstillingene vil overstyre arbeidsflytinnstillingene.

De tilgjengelige feltene er:

| Felt | Beskrivelse |
| --- | --- |
| `Antall dager før forfall` | Antall dager siden siste oppdatering av en sak før den anses som forfalt. |
| `Frekvens for påminnelses-e-post` | Frekvensen for å sende forfalte e-postvarsler, med alternativer som `Av`, `Hver dag`, `Hver mandag`, osv. |
| `Tidspunkt på dagen for å sende forfalte e-poster` | Angir tidspunktet på dagen for å sende e-posten. For eksempel kan du ønske at forfalte varsler blir levert etter klokken 9 om morgenen. Dette er ikke en eksakt tid; e-posten vil bli sendt en gang etter angitt tid, avhengig av e-postsystemet ditt og sendetid. |

### Eskalering

Denne funksjonen lar deg styre hvordan eskaleringer håndteres. Det lar deg angi generelle innstillinger for håndtering av eskaleringer for en arbeidsflyt, som vil gjelde for alle `skjemaer` som bruker den arbeidsflyten.

> `Skjemaer` lar deg overstyre disse innstillingene. For eksempel kan du ha et `Ulykkes`-skjema med mye kortere automatiske eskalertider sammenlignet med den generelle arbeidsflyten. `Skjema`-innstillingene vil overstyre arbeidsflytinnstillingene.

De tilgjengelige feltene er:

| Felt | Beskrivelse |
| --- | --- |
| `Eskalering av forfalte saker aktivert` | Aktiverer eller deaktiverer eskaleringsfunksjonen. |
| `Eskaler etter N timer forfalt` | Antall timer siden siste sakoppdatering før den anses for eskalering. |
| `Eskaleringsstrategi` | Strategien som brukes for å bestemme til hvem saken skal eskaleres. Se tilgjengelige strategier nedenfor. |
| `Tidspunkt på dagen for å eskalere meldinger` | Tidspunktet på dagen når meldinger skal eskaleres. |
| `Antall timer for neste forfallsdato etter eskalering` | Neste forfallsdato etter å ha eskalert saken til en ny saksbehandler. |

De tilgjengelige strategiene er:

| Strategi | Beskrivelse |
| --- | --- |
| `Direkte overordnet` | Saken vil bli sendt til personens nærmeste direkte overordnede med tillatelse til å behandle saker. Hvis det er flere potensielle overordnede, vil en av dem bli valgt tilfeldig. |