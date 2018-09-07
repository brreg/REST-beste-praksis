# 02 Bruk webstandarder som fundament for API'et

Design API'er med hensyn til web-standarder
## Hvorfor
API'er basert på web-standarder utnytter styrken i web'en. For eksempel, vil å bruke HTTP-verb som metoder og URI'er som mapper direkte til ressurser vil hjelpe å unngå tette koblinger mellom requester og responser, som igjen kan medføre at API'et blir enklere å forstå og bruke. Tilstandsløsheten kan gi fordeler med tanke på skalerbarhet, og hypermedia muliggjør rike interaksjoner med API'et.
## Tiltenkt utfall
Utviklere med erfaring ved bruk av API'er basert på web-standarder, som REST, vil ha en basisforståelse for hvordan API'et kan brukes. API'et vil også bli enklere å vedlikeholde.
## Forslag til implementasjon
Implementere API'et ved hjelp av REST og HATEOAS.
Eksempel: Bruk korrekte REST-verb for operasjoner

| HTTP verb     | CRUD          |
| ------------- |---------------|
| GET           | Les           |
| POST          | Opprett       |
| PUT           | Oppdater      |
| DELETE        | Slett         |
| PATCH         | Oppdater      |
| HEAD          | Sjekk headere |

Eksempel: Bruk standard http status koder
Ref https://httpstatuses.com/

Eksempel: Bruk standard media types i beskrivelsen av innhold
https://www.iana.org/assignments/media-types/media-types.xhtml
## Eksempler
## Hvordan teste
## Gevinster
