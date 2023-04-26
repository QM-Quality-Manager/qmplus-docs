---
title: "Administrator/Arbeidsflyter"
description: "En brukerveiledning for arbeid med arbeidsflyter"
lead: "En brukerveiledning for arbeid med arbeidsflyter. Vi dekker hvordan du oppretter og endrer arbeidsflyter."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 27
toc: true
---

Denne delen handler om å administrere arbeidsflyter i systemet.

Ved å klikke på `Administrator/Arbeidsflyter` får du tilgang til listen over arbeidsflyter.

## Liste over arbeidsflyter

{{< figure src="/images/workflows/workflows_1.png" caption="Liste over arbeidsflyter" width="1024">}}

Oversikten over arbeidsflytlistene lar deg se alle arbeidsflyter definert i systemet. Arbeidsflyter er globale og deles av alle avdelinger i organisasjonen.

Arbeidsflyter kan aktiveres og deaktiveres etter behov. Dette påvirker ikke eksisterende `skjema typer` som bruker arbeidsflyten, men gjør det umulig å lage nye `skjema typer` for den spesifikke arbeidsflyten.

## Opprette arbeidsflyt

{{< figure src="/images/workflows/workflows_2.png" caption="Opprette en arbeidsflyt" width="1024">}}

Det er fire faner å vurdere når du oppretter en ny arbeidsflyt.

| Fane | Beskrivelse |
| --- | --- |
| `Generelt` | Angi generelle detaljer for arbeidsflyten. |
| `Tabell` | Rediger statusene, overgangene og dialogene som utgjør arbeidsflyten. |
| `Graf` | En grafisk fremstilling av arbeidsflyten. |
| `Behandling` | Standard innstillinger for behandling av arbeidsflyten, som automatiske frister osv. |

### Generell fane

Den generelle siden lar oss fylle ut følgende felt.

{{< figure src="/images/workflows/workflows_12.png" caption="Generell fane" width="1024">}}

| Felt | Beskrivelse |
| --- | --- |
| `Tittel` | Angi tittelen på arbeidsflyten; støtter flere språk hvis kontoen din er konfigurert for det. |
| `Entitetstype` | Velg entitetstypen for arbeidsflyten; når den er satt, kan den ikke endres. Dette kan være `Melding`, `Handling`, `Dokument`, `Høring` eller `Revisjon`. |
| `Deaktiver overgangskontroll` | Dette lar deg overstyre eventuelle overganger, noe som gjør det mulig å flytte saker fritt mellom eventuelle overganger på saksbrettet. Flott for å implementere Kanban-prosesser eller andre ikke-gatede prosesser. |
| `Start sakstatus` | Angi standard startstatus for saken. Dette er sakstatusen som vil bli tildelt en ny sak for denne arbeidsflyten hvis ingen andre regler overstyrer den. |
| `Lukk sakstatus` | Angi standard lukket sakstatus som brukes for standard lukkeoperasjoner. |
| `Tidlig sakprosess` | Angi at denne arbeidsflyten støtter bruk av `Tidlig sakprosess`-regler som er satt opp for å tildele nye saker til saksbehandlere basert på angitte regler. |
| `Assosiert revisjonsarbeidsflyt` | `Dokument only`. Lar deg angi en assosiert revisjonsarbeidsflyt for denne dokumentarbeidsflyten for å håndtere alle høringer. |

### Tabellfane

{{< figure src="/images/workflows/workflows_3.png" caption="Tabellfane" width="1024">}}

Tabellfanen lar oss bygge og endre arbeidsflytentitetene. Det er tre typer tilgjengelige enheter.

| Enheter | Beskrivelse |
| --- | --- |
| `Sakstatus` | Sakstatus er definerte tilstander en sak kan være i. For eksempel kan du ha en sakstatus kalt `Ny` for en nyregistrert skjemapost og `Lukket` for den endelige mulige tilstanden for en sak. |
| `Overganger` | Overganger styrer flyten av saker mellom sakstatus. Det gjør det mulig å håndheve en arbeidsflyt ved å angi lovlige overganger mellom statusene. For eksempel kan du gjøre det mulig å bare flytte en sak fra `Ny` til `Under arbeid` ved å legge til en enkelt overgang mellom disse statusene. |
| `Dialoger` | Dialoger er samlinger av felt som kan kobles til en overgang. For eksempel kan du bestemme at du vil at brukeren skal legge til en kommentar når du flytter en sak fra sakstatus `Ny` til `Under arbeid`, og en dialog som er knyttet til denne overgangen mellom disse feltene, vil be om at dialogen dukker opp for brukeren å fylle ut når du flytter mellom statusene. |

### Opprett status

{{< figure src="/images/workflows/workflows_4.png" caption="Opprett ny arbeidsflytstatus" width="1024">}}

For å opprette en ny `Sakstatus` må du angi følgende felt.

| Felt | Beskrivelse |
| --- | --- |
| `Navn` | Navnet på sakstatusen, som støtter flere språk. |
| `Statusgruppe` | Statusgruppen for denne sakstatusen (se tabellen nedenfor for forklaringer). |
| `Beskrivelse` | En valgfri beskrivelse for sakstatusen. |

De mulige `Statusgruppene` er beskrevet nedenfor.

| Statusgruppe | Beskrivelse |
| --- | --- |
| `Åpen` | En sak er i en nyåpnet tilstand (første gang den ble åpnet). Dette brukes først og fremst for å signalisere en ny sak som starter. |
| `Ubearbeidet` | En sak er opprettet, men ikke ennå åpnet av noen saksbehandler. |
| `Under arbeid` | En sak blir arbeidet med. |
| `I handlingsprosess` | En sak utløste en handlingsprosess og venter på at den skal løses. |
| `Lukket` | En sak er lukket. |
| `Slettet` | En sak er slettet. |

### Opprett overganger

{{< figure src="/images/workflows/workflows_5.png" caption="Opprett arbeidsflytovergang" width="1024">}}

En overgang representerer en endring mellom to statuser (for eksempel kan du flytte en sak fra `Ny`-status til `Under arbeid`-status).

En overgang kan ha en valgfri dialog knyttet til den for å samle informasjon som en del av overgangen.

> Når vi snakker om overganger, vil vi bruke `kilde` som startstatus for overgangen og `mål` som sluttstatus.

Vi har følgende felter når vi oppretter en overgang.

| Felt | Beskrivelse |
| --- | --- |
| `Overgangsnavn` | Navnet på overgangen vi definerer. |
| `Fra status` | Start-`Sakstatus` for overgangen. |
| `Til status` | Slutt-`Sakstatus` for overgangen. |
| `Dialog` | En valgfri dialog knyttet til overgangen. |
| `Relatert arbeidsflyt` | Når man overgår til en `Sakstatus` i statusgruppen `I handlingsprosess`, kan vi angi en relatert arbeidsflyt som vil bli brukt til å utløse opprettelsen av en ny `Handling` når denne overgangen utføres. Dette alternativet er for øyeblikket bare tilgjengelig for `Meldingsarbeidsflyter`. |
| `Startstatus` | Angi hvilken status en nylig opprettet `Handling` skal ha i den `Relaterte arbeidsflyten`. |

> Alternativet Relatert arbeidsflyt brukes bare når `Til status` er en `Sakstatus` i statusgruppen `I handlingsprosess`.

### Opprett dialog

{{< figure src="/images/workflows/workflows_6.png" caption="Opprett arbeidsflytdialog" width="1024">}}

En dialog representerer et sett med felt som kan konfigureres av sluttbrukeren for å samle inn informasjon eller utløse handlinger ved en endring av status for en sak (en overgang). Dialoger er knyttet til overganger.

Feltene du kan angi er som følger:

| Felt | Beskrivelse |
| --- | --- |
| `Dialognavn` | Navnet på arbeidsflytdialogen, støtter flere språk. |
| `Beskrivelse` | En valgfri beskrivelse for dialogen. |
| `Felt` | Listen over felt som brukes i dialogen. |

Som du kan se, er det et betydelig utvalg av felttyper. La oss undersøke hver og forstå deres betydning før vi konstruerer vår tilpassede dialog.

| Felttype | Utgangspunkt | Beskrivelse |
| --- | --- | --- |
| `Tekstfelt` | Nei | Et enkelt-rad fritekst inntastingsfelt. |
| `Tekstområde` | Nei | Et tekstområde med flere kolonner for fritekst inntasting. |
| `Tekstredigerer` | | Et tekstområde med grunnleggende formatering for fritekst inntasting. |
| `Tall` | Nei | Lar deg skrive inn et hvilket som helst numerisk verdi. |
| `Dato` | Nei | Brukes til å spesifisere en dato. |
| `Utfør oppgave` | Ja | Et felt som lar deg angi hvem som utførte oppgaven. |
| `Handlingens navn` | Ja | Tittelfeltet som vil bli brukt når man oppretter en ny `Handling`-oppføring for en overgang som går inn i en `I handlingsprosess`-gruppetilstand. |
| `Kommentar` | Ja | Lar brukeren kommentere overgangen mellom tilstander og angi hvem som skal få varsel om kommentaren. |
| `Bekreftelse` | Ja | Lar brukeren bekrefte at spesifikke brukere har utført sine oppgaver. |
| `Oppgavetildelingsoppsett` | Ja | Lar brukeren opprette oppgaver av en bestemt type når man går mellom statuser. Man kan også kontrollere om man ønsker å samle inn en `Forfallsdato`, `Planlagte timer`, og `Planlagt startdato`. |

{{< figure src="/images/workflows/workflows_11.png" caption="Legge til felter i dialog" width="1024">}}

Du kan legge til felter i dialogen og se forhåndsvisningen av dialogen på venstre side. Når du har spesifisert alle feltene, kan du klikke på `Lagre endringer`-knappen nederst til høyre for å lagre endringene i arbeidsflyten.

### Graf-fane

{{< figure src="/images/workflows/workflows_7.png" caption="Graf-fane" width="1024">}}

`Graf-fanen` viser en grafisk fremstilling av arbeidsflyten. Hver boks representerer en `Sakstatus` i arbeidsflyten, og hver linje mellom `Sakstatusene` representerer en overgang mellom to tilstander. Arbeidsflyten over er veldig enkel; nedenfor er et mer komplekst eksempel på en arbeidsflyt.

{{< figure src="/images/workflows/workflows_10.png" caption="Eksempelgraf" width="1024">}}

> Bruk `Graf-fanen` for å validere arbeidsflyten din og forsikre deg om at du ikke har gått glipp av noen overganger. En `Sakstatus` uten overganger er et typisk signal om at man kanskje har gått glipp av en overgang, eller at `Sakstatusen` ikke er nødvendig.

### Behandlingsfane

Behandlingsfanen inneholder innstillinger for å sette standarder for saksfrister og eskaleringer for alle skjematyper og skjemaer knyttet til denne spesifikke arbeidsflyten.

{{< figure src="/images/workflows/workflows_8.png" caption="Behandlingsfane" width="1024">}}

#### Forfallsdatoer

Gir kontroll over hvordan forfallsdato-varsler håndteres. Dette lar deg sette generelle innstillinger for håndtering av forfallsdatoer for denne arbeidsflyten og dermed `skjemaer` som bruker denne arbeidsflyten.

> `Skjemaer` lar deg overstyre disse, slik at du for eksempel kan ha et skjema `Ulykke` med mye kortere automatiske forfallsdatoer sammenlignet med den generelle arbeidsflyten. `Skjema`-innstillinger vil overstyre arbeidsflyten.

De tilgjengelige feltene.

| Felt | Beskrivelse |
| --- | --- |
| `Antall dager før forsinket` | Antall dager siden siste oppdatering av en sak før den anses som forsinket. |
| `Påminnelsesepost-frekvens` | Frekvensen for å sende forsinkede e-postvarsler. Dette er alternativer som `Av`, `Hver dag`, `Hver mandag`, osv. |
| `Tidspunkt på dagen for å sende forsinkede e-poster` | Angi tidspunktet på dagen for å sende e-posten. For eksempel kan du ønske at forsinkede meldinger leveres etter kl. 9 om morgenen. Dette er ikke en eksakt tid. E-posten vil bli sendt en gang etter angitt tid, avhengig av e-postsystemet og sendetiden. |

#### Eskalering

Gir kontroll over hvordan eskaleringer håndteres. Dette lar deg sette generelle innstillinger for håndtering av eskaleringer for denne arbeidsflyten og dermed `skjemaer` som bruker denne arbeidsflyten.

> `Skjemaer` lar deg overstyre disse, slik at du for eksempel kan ha et skjema `Ulykke` med mye kortere automatiske eskaleringsdatoer sammenlignet med den generelle arbeidsflyten. `Skjema`-innstillinger vil overstyre arbeidsflyten.

De tilgjengelige feltene.

| Felt | Beskrivelse |
| --- | --- |
| `Eskalering av forsinkede saker aktivert` | Aktiver eller deaktiver eskaleringen. |
| `Eskaler etter N timer forsinket` | Antall timer siden siste sakoppdatering skjedde før den vurderes for eskalering. |
| `Eskaleringsstrategi` | Strategien for å velge hvem saken skal eskaleres til. Se tilgjengelige strategier nedenfor. |
| `Tidspunkt på dagen for å eskalere meldinger` | Hva tid på dagen for å eskalere meldinger. |
| `Antall timer for neste forfallsdato etter eskalering` | Neste forfallsdato etter å ha eskalert saken til en ny saksbehandler. |

De tilgjengelige strategiene.

| Strategi | Beskrivelse |
| --- | --- |
| `Direkte overordnet` | Saken vil bli sendt til personens nærmeste direkte overordnede med tillatelse til å behandle saker. Hvis det er mer enn én potensiell overordnet, vil en av dem bli valgt tilfeldig. |
| `Tidspunkt på dagen for å sende forsinkede e-poster` | Angi tidspunktet på dagen for å sende e-posten. For eksempel kan du ønske at forsinkede meldinger leveres etter kl. 9 om morgenen. Dette er ikke en eksakt tid. E-posten vil bli sendt en gang etter angitt tid, avhengig av e-postsystemet og sendetiden. |

#### Eskalering

Gir kontroll over hvordan eskaleringer håndteres. Dette lar deg sette generelle innstillinger for håndtering av eskaleringer for denne arbeidsflyten og dermed `skjemaer` som bruker denne arbeidsflyten.

> `Skjemaer` lar deg overstyre disse, slik at du for eksempel kan ha et skjema `Ulykke` med mye kortere automatiske eskaleringsdatoer sammenlignet med den generelle arbeidsflyten. `Skjema`-innstillinger vil overstyre arbeidsflyten.

De tilgjengelige feltene.

| Felt | Beskrivelse |
| --- | --- |
| `Eskalering av forsinkede saker aktivert` | Aktiver eller deaktiver eskaleringen. |
| `Eskaler etter N timer forsinket` | Antall timer siden siste sakoppdatering skjedde før den vurderes for eskalering. |
| `Eskaleringsstrategi` | Strategien for å velge hvem saken skal eskaleres til. Se tilgjengelige strategier nedenfor. |
| `Tidspunkt på dagen for å eskalere meldinger` | Hva tid på dagen for å eskalere meldinger. |
| `Antall timer for neste forfallsdato etter eskalering` | Neste forfallsdato etter å ha eskalert saken til en ny saksbehandler. |

De tilgjengelige strategiene.

| Strategi | Beskrivelse |
| --- | --- |
| `Direkte overordnet` | Saken vil bli sendt til personens nærmeste direkte overordnede med tillatelse til å behandle saker. Hvis det er mer enn én potensiell overordnet, vil en av dem bli valgt tilfeldig. |