---
term: BIP42

---
Ehdotus Bitcoin Coren parantamiseksi, joka korjaa pienen virheen lohkopalkkioiden vähennysaikataulussa. Jos tämä poikkeama olisi jätetty korjaamatta, se olisi johtanut siihen, että bitcoinien kokonaismäärä olisi ylittänyt suunnitellun 21 miljoonan bitcoinin rajan. Tarkemmin sanottuna, puolikkaiden päättymisen jälkeen uusi bitcoinien luomisen sykli olisi teoriassa voinut käynnistyä vuoden 2214 tienoilla. Kyseinen Core-koodi käytti oikeaa binäärisiirto-operaatiota louhijan palkkion arvoon. Virhe johtui tämän siirto-operaation käytöstä tilanteessa, jossa käyttäytyminen oli C++-kielen standardien mukaan määrittelemätöntä. 64-bittisen kokonaisluvun (`int64_t`) siirtäminen yli 63 bittiä oikealle kuuluu tähän määrittelemättömän käyttäytymisen kategoriaan. Bitcoin Core -koodissa tämä olisi voinut tapahtua 64 halvingin jälkeen, lohkon korkeudella nro 13 440 000. Tämän rajan jälkeen bittisiirron käyttäytymistä ei ollut määritelty, mikä tarkoittaa, että eri kääntäjät saattoivat tulkita koodia eri tavoin. Tämä olisi voinut johtaa arvaamattomiin lopputuloksiin, mukaan lukien äärettömän bitcoin-inflaation luomisen mahdollisuus. BIP42 korjasi tämän ongelman määräämällä, että lohkopalkkio asetetaan nollaan 64 puolikkaan jälkeen, jolloin vältettiin oikean siirto-operaation käyttö määrittelemättömän käyttäytymisen yhteydessä. Tämä muutos, joka oli pehmeä haarautuminen, selkeytti näin Bitcoin Core -koodin käyttäytymistä. Vaikka tämä BIP42:n korjaama virhe oli varsin vakava, se ei ollut välittömästi kriittinen, sillä se olisi ilmennyt vasta noin vuonna 2214. Pieter Wuillen 1. huhtikuuta 2014 julkaisema BIP42 erottuu siten humoristisesta sävystään.