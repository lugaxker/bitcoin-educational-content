---
term: HERDET AVLEDNING

---
Prosessen med å generere underordnede nøkler i HD-lommebøker. Herdet avledning bruker den overordnede private nøkkelen som input for `HMAC-SHA512`-funksjonen, noe som gjør det umulig å generere underordnede offentlige nøkler fra den overordnede offentlige nøkkelen og den overordnede kjedekoden. Prosessen innebærer å sammenkoble den overordnede private nøkkelen og en indeks som er større enn eller lik $2^{31}$, etterfulgt av anvendelsen av `HMAC-SHA512` med den overordnede kjedekoden. Resultatet deles i to deler: De første 256 bitene legges til den overordnede private nøkkelen for å få den underordnede private nøkkelen, mens de resterende 256 bitene danner den underordnede kjedekoden. Denne metoden sikrer at selv om en utvidet offentlig nøkkel blir kompromittert, kan den ikke brukes til å utlede underordnede offentlige nøkler. I standard avledning brukes herdet avledning på alle avledningsnivåer opp til kontodybden. I avledningssti-notasjoner identifiseres en herdet avledning med en apostrof `'` eller, mer sjelden, med en `h`.