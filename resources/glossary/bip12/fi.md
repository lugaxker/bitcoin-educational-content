---
term: BIP12

---
Gavin Andresenin ehdotus Bitcoin-tapahtumien skriptien joustavuuden ja yksityisyyden suojan parantamiseksi. Tässä BIP:ssä ehdotetaan, että otetaan käyttöön uusi skriptin op-koodi nimeltä `OP_EVAL`, joka mahdollistaa skriptin `scriptSig` tietoihin sisältyvän skriptin arvioinnin transaktion validointiprosessin aikana. BIP12:n tärkein muutos on sallia yhden skriptin sisällyttäminen toisen skriptin sisälle. Tämä tekniikka mahdollistaa monimutkaisempien ehtojen luomisen, jotka voidaan tarkistaa rahankäytön yhteydessä ilman, että niitä tarvitsee paljastaa käyttäjille, jotka lähettävät bitcoineja käytettyyn osoitteeseen. BIP12 korvattiin myöhemmin turvallisemmilla ehdotuksilla, erityisesti BIP16:lla (P2SH), joka tarjoaa erilaisen menetelmän samojen tavoitteiden saavuttamiseksi kuin "OP_EVAL".