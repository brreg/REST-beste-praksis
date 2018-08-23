# 01 Lag spesifikasjon for API'et

Tilby komplett spesifikasjon på Web om ditt API. Oppdater spesifikasjonen før man legger til nye egenskaper eller gjør endringer.
## Hvorfor
Utviklere er primærkonsumenter av et API og spesifikasjonen er et av de første hjelpemidlene for å kunne si noe om API'ets kvalitet og brukbarhet. Når API spesifikasjonen er fullstendig og lett å forstå, vil utviklere være mer villig til å fortsette å bruke det. Å tilby utfyllende og komplett spesifikasjon på ett sted, gir utviklere muligheten til å kode effektivt. Å tydelig markere endringer, gir brukerne mulighet til å ta i bruk nye endringer og tilpasse sin kode hvis nødvendig.
## Tiltenkt utfall
Brukere vil kunne hente informasjon om hvert kall til API'et, inkludert parametrene det kan ta og hva man kan forvente i retur.
Man bør være i stand til å finne ut hvordan man bruker API'et, få beskjed om enringer, kontaktinformasjon osv.
API'et bør være beskrevet og enkelt å finne og bruke.
## Forslag til implementasjon
Spesifikasjonen skal være i henhold til [OpenAPI-Specification versjon 3.x](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.1.md) representert i YAML-format. Spesifikasjonen skal ha samme navnet som API-et.

Man skal beskrive:
* En komplett liste av kallene et API kan håndtere
* Hensikten med hvert av kallene
* Detaljere parametrene det tillater og hva det returnerer
* Gi ett eller flere eksempler på bruk
* Eventuelle feilsituasjoner
* Eventuell autentisering

## Eksempler:
* https://data.brreg.no/oppgaveregisteret/docs/api.html
* https://raw.githubusercontent.com/Informasjonsforvaltning/example-api/master/app/openAPI/industrialcodes_3.0.yaml

## Hvordan teste
Ideelt sett bør man genere automatiserte tester som tester API'et basert på spesifikasjonen.
Sjekk at alle kall som tilbys fra ditt API er beskrevet i spesifikasjonen. Verifiser at man tilbyr detaljer om hvilke parametre er påkrevd og hva som returneres.
Sørg for at man har en akseptabel Time To First Successful Call (være i stand til å gjøre en akseptert forespørsel til API'et innen noen minutt), for å gjøre det mer attraktivt å fortsatt bruke API'et.
Verifiser for hver endring at spesifikasjonen er korrekt.
## Gevinster
