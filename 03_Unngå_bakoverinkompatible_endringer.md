# 03 Unngå bakoverinkompatible endringer

Unngå endringer til API'et som kan knekke klientkoden, og kommuniser alle endringer i API'et til utviklerne når endringene skjer
## Hvorfor
Når en utvikler implementerer en klient mot vårt API kan de være avhengige av egenskaper vi har bygd inn i dette, som f.eks. skjema eller responsformat. Ved å unngå bakoverinkompatible endringer kan vi minimalisere feil i klientkoden.
Ved å kommunisere godt ut mot bruker, vil disse kunne ta i bruk nye features, og i de sjeldne tilfellene hvor brudd skjer, kunne gjøre noe med dette.
## Tiltenkt utfall
Klientkode vil fortsatt fungere etter endringer. Utviklere vil vite om forbedringer vi gjør, og vil være i stand til å utnytte disse. Bakoverinkompatible endringer vil være sjeldne, og hvis de oppstår vil utviklere ha tilstrekkelig med tid og informasjon til å endre sin egen kode. Dette vil gjøre dem i stand til å unngå feil, og dermed oppnå større tillitt. Endringer i API'et bør informeres om der dokumentasjonen finnes.
## Forslag til implementasjon
Legg til nye tjenester og variasjoner, fremfor å endre hvordan eksisterende kall fungerer. Eksisterende klienter kan ignorere disse og fortsatt fungere.
Hold URI konstant, og endre kun det som ikke kan kodes mot direkte.
Hvis endringene som må gjøres likevel ikke lar seg gjennomføre uten å innføre endringer av denne sort, så må man enten lansere ny tjeneste, eller ta i bruk versjonering.
Eksempel på endringer som kan knekke klientkode:
* Fjerne en tjeneste
* Endre URI av en ressurs
* Endre REST-verb, feks GET->PUT
* Legge til parameter
* Endre datatype på parameter eller respons
* Endre strukturen på en XML-respons
Det anbefales å tilby måter å informere bruker direkte. RSS er en måte hvor bruker kan bli informert uten å indentifisere seg. Det anbefales også å tilby et forum for å tilby to-veis-kommunikasjon. Det er vanskelig å tilby dette anonymisert.
## Eksempler
## Hvordan teste
Rull ut endringene til en test-versjon av API'et som klienter har tilgang til. Tilby utviklere å teste mot denne versjonen og gi tilbakemeldinger før versjonen rulles ut til produksjon.
## Gevinster
