# 04 Bruk content negotiation for å tilby data på multiple format

Bruk content negotiation  for å tilby data på multiple format
## Hvorfor
En ressurs kan representeres gjennom mange format, f.eks. JSON, XML, CSV, HTMl. Gjennom content negotiation kan alle formatene (inkludert versjoner) være tilgjengelig fra samme URL.

## Tiltenkt utfall
Content negotiation gjør det mulig å ha tilby forskjellige representasjoner av ressursen avhengig av hva klienten ber om.
## Forslag til implementasjon
Konfigurer web-server til å håndtere content negotiation av en ressurs.
Eksempel:
```
curl -H "Accept: text/csv" http://data.brreg.no/enhetsregisteret/enhet/980123456
```
## Eksempler
## Hvordan teste
Sjekk at de forskjellige representasjonene er tilgjengelig ved å spesifisere accepted content i HTTP Request header.
## Gevinster
