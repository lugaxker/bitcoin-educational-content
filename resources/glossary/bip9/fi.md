---
term: BIP9

---
Vuonna 2015 ehdotettu menetelmä Bitcoinin pehmeiden haarojen aktivoimiseksi. Siinä otetaan käyttöön järjestelmä, jossa louhijat ilmoittavat tukevansa pehmeää haarautumista käyttämällä tiettyä bittiä lohkojen versiokentässä. BIP9:n mukaisesti ehdotettu pehmeä haarautuminen aktivoituu, jos 95 prosenttia lohkoista vuoden 2016 lohkojen aikana (noin kaksi viikkoa, joka osuu yhteen jokaisen vaikeusasteen muutoksen kanssa) ilmoittaa hyväksyntänsä. Tämän lukituksen jälkeen kaivostyöläisille annetaan armonaika valmistautua päivitykseen ennen sen aktivointia. Jos 95 prosentin kynnysarvoa ei saavuteta annetussa enimmäisajassa, soft fork hylätään. BIP9 mahdollistaa useiden soft fork -haarojen signaloinnin samanaikaisesti, mutta antaa kaivostyöläisille huomattavan paljon valtaa, sillä jos vaadittua kynnysarvoa ei saavuteta, soft fork yksinkertaisesti hylätään. Tätä menetelmää käytettiin alun perin SegWitissä, ennen kuin BIP148, jossa ehdotetaan UASF:n käyttöä, tuli käyttöön ja pakotti lukituksen BIP91:n avulla.