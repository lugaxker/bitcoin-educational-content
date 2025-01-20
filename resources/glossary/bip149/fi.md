---
term: BIP149

---
Shaolin Fryn ehdotus SegWitin (BIP141, BIP143 ja BIP147) uudesta käyttöönotosta BIP8-aktivointimenetelmällä, jossa on "LOT=true", jos SegWitin alkuperäinen käyttöönotto BIP9:n kautta ei aktivoitunut ennen 15. marraskuuta 2017. Toisin kuin BIP9-menetelmässä, jossa signalointivirhe johtaa aktivoinnin hylkäämiseen, BIP149:n tavoitteena oli aktivoida SegWit 4. heinäkuuta 2018 riippumatta siitä, saavuttivatko louhijat 95 prosentin signalointikynnyksen vai eivät. Marraskuun ja heinäkuun välisen kahdeksan kuukauden jakson aikana solmuilla olisi ollut mahdollisuus toteuttaa BIP149, jotta verkon taloudellinen enemmistö olisi voinut varmistaa SegWitin aktivoinnin, jos louhijoiden aktivointia ei olisi tapahtunut (UASF). Kun ensimmäinen vaikeusasteen säätö olisi saavutettu 4. heinäkuuta 2018 jälkeen, aktivointi olisi siirtynyt tilaan `LOCKED_IN`, ja SegWit olisi aktivoitu seuraavassa säätöjaksossa. Toisin kuin BIP148:ssa, jossa suunniteltiin SegWit-aktivointia, jonka käyttäjät tai kaivostyöläisten enemmistö pakottaisivat, BIP149 ehdotti asteittaisempaa ja maltillisempaa aktivointimenetelmää, vaikkakin se pysyi edelleen selvästi hyökkäävänä, BIP8:n periaatteiden mukaisesti. BIP148 ennakoi konfliktia lohkoketjun jakautumisen kanssa, mutta BIP149 vältti tämän mahdollisuuden hyväksymällä lohkot, jotka eivät anna SegWit-merkkiä, paitsi jos louhija tekee sen tietoisesti (ilman kannustinta). Näin ollen BIP149 oli BIP148:aa vähemmän konfliktialtis SegWit-aktivointimekanismi, joka suosi järjestelmän asteittaisempaa ja riskittömämpää käyttöönottoa. BIP148:aa tai BIP149:ää ei lopulta toteutettu, vaan SegWit aktivoitiin MASF:n kautta, erityisesti BIP91:n sysäyksenä.