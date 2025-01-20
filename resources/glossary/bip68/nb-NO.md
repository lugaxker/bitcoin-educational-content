---
term: BIP68

---
Innført muligheten til å bruke relative låsetider gjennom feltet `nSequence`. Dette gjør det mulig for en transaksjon å angi en relativ forsinkelse før den kan inkluderes i en blokk. Denne forsinkelsen kan defineres i form av antall blokker eller som et multiplum av 512 sekunder (dvs. sanntid). Merk at denne nye tolkningen av feltet `nSequence` bare er gyldig hvis feltet `nVersion` er større enn eller lik `2`. Denne tolkningen av `nSequence`-feltet skjer på nivået av Bitcoins konsensusregler. Den relative tidslåsen angir en forsinkelse fra aksept av en tidligere transaksjon, mens den absolutte tidslåsen angir et nøyaktig tidspunkt før transaksjonen ikke kan inkluderes i en blokk. BIP68 ble introdusert via en soft fork 4. juli 2016, sammen med BIP112 og BIP113, som for første gang ble aktivert ved hjelp av BIP9-metoden.