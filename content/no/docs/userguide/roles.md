---
title: "Administrator/Brukertillatelser"
description: "En brukerveiledning for arbeid med brukertillatelser"
lead: "En brukerveiledning for arbeid med brukertillatelser. Vi dekker hvordan du oppretter og endrer brukertillatelser."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "tutorials"
weight: 8
toc: true
---
Denne delen omhandler administrasjon av brukertilgang i systemet.

Ved å klikke på `Administrator/Brukertillatelser`, får du tilgang til listen over alle tilgjengelige tillatelser.

Det er to typer tillatelser i systemet:

| Type | Beskrivelse |
| --- | --- |
| `System` | Systemtillatelser kontrollerer tilgang til seksjoner eller handlinger innenfor applikasjonen selv og leveres av applikasjonen. For eksempel kan disse tillatelsene tillate deg å administrere brukere eller vise rapporter. Brukere kan ikke tilpasse disse tillatelsene, og de kan utvides når nye funksjoner blir lagt til. |
| `Egendefinert` | Egendefinerte tillatelser er tillatelser som brukere kan opprette for å merke innhold, som dokumenter, eller begrense tilgang til bestemte områder som avdelinger. For eksempel kan du ha et `konfidensielt` dokument som bare to personer skal ha tilgang til. I så fall kan du opprette en `konfidensielt dokument` egendefinert tillatelse og tilordne den til dokumentet og de to brukerne du ønsker å gi tilgang til. Fravær av tillatelsen vil forhindre brukere i å få tilgang til dokumentet. |

[Se alle tilgjengelige System Permissions]({{< ref "/content/no/docs/references/permissions.md" >}} "System Permissions")

## Tillatelsesliste

### Systemtillatelser

{{< figure src="/images/user_permissions/user_permissions_1_no.png" caption="Systemtillatelser liste" width="1024">}}

Bildet ovenfor viser listen over `Systemtillatelser`. Du kan filtrere disse tillatelsene for å søke etter spesifikke. `Systemtillatelser` kan ikke endres eller slettes, og de representerer alle `Applikasjonsnivå tillatelser` tilgjengelige for kontoen din. Antallet tilgjengelige tillatelser kan variere avhengig av kontraktsalternativene dine.

En komplett liste over `Systemtillatelser` finnes her.

### Egendefinerte tillatelser

{{< figure src="/images/user_permissions/user_permissions_2_no.png" caption="Egendefinerte tillatelser liste" width="1024">}}

Egendefinerte tillatelser er tillatelser som brukere kan opprette for å merke innhold, som dokumenter, eller begrense tilgang til områder som avdelinger. For eksempel kan du ha et `konfidensielt` dokument som bare to personer skal ha tilgang til. I så fall kan du opprette en `konfidensielt dokument` egendefinert tillatelse og tilordne den til dokumentet og de to brukerne du ønsker å gi tilgang til. Fravær av tillatelsen vil forhindre brukere i å få tilgang til dokumentet.

## Opprett egendefinert tillatelse

{{< figure src="/images/user_permissions/user_permissions_3_no.png" caption="Opprett ny egendefinert tillatelse-visning" width="1024">}}

Når du oppretter en egendefinert tillatelse, må du oppgi:

1. Et tillatelsesnavn (på flere språk hvis systemet ditt støtter mer enn ett språk).
2. Synligheten til tillatelsen i systemet.
3. `Avdelingen` der tillatelsen eksisterer.

Til slutt, klikk på `Opprett ny tillatelse`-knappen for å lagre den nye egendefinerte tillatelsen.