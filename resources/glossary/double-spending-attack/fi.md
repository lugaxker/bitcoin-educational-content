---
term: (HYÖKKÄYS)

---
Hyökkäys, jossa pahantahtoinen käyttäjä yrittää käyttää samaa UTXO:ta (*Unspent Transaction Output*) useammin kuin kerran rikastuakseen transaktioihin osallistuvien osapuolten kustannuksella. Periaatteessa, kun transaktio on vahvistettu lohkossa ja lisätty lohkoketjuun, kyseisten bitcoinien käyttö kirjataan pysyvästi, mikä estää samojen bitcoinien käyttämisen uudelleen. Kaksinkertaisen käytön estäminen on jopa lohkoketjun ensisijainen hyöty.

Kaksinkertaisen rahankäytön hyökkäyksen yhteydessä hyökkääjä tekee ensin laillisen maksutapahtuman kauppiaan kanssa ja luo sitten toisen kilpailevan maksutapahtuman, jossa hän käyttää samoja kolikoita joko lähettämällä ne takaisin itselleen saadakseen summan takaisin tai käyttämällä niitä toisen tavaran tai palvelun ostamiseen eri kauppiaalta.

Tämä hyökkäys voi tapahtua kahdessa eri tilanteessa. Ensimmäisessä ja hyökkääjän kannalta yksinkertaisimmassa tapauksessa vilpillinen transaktio suoritetaan ennen kuin laillinen transaktio sisällytetään lohkoon. Varmistaakseen, että vilpillinen transaktio vahvistetaan ensin, hyökkääjä liittää siihen huomattavasti korkeammat transaktiomaksut kuin lailliseen transaktioon. Tämä on eräänlainen petollinen RBF. Tämä skenaario on mahdollinen vain, jos kauppias suostuu viimeistelemään myynnin "zeroconfissa" eli ilman maksutapahtuman vahvistuksia. Tämän vuoksi on erittäin suositeltavaa odottaa useita vahvistuksia, ennen kuin tapahtumaa pidetään muuttumattomana. Toinen, paljon monimutkaisempi skenaario on 51 prosentin hyökkäys. Jos hyökkääjä hallitsee merkittävää osaa verkon laskentatehosta, hän voi louhia kilpailevan ketjun, joka sisältää laillisen maksutapahtuman, mutta sisältää myös hänen vilpillisen maksutapahtumansa. Kun kauppias on hyväksynyt kaupan ja hyökkääjä on onnistunut luomaan pidemmän ketjun (jossa on enemmän kertynyttä työtä) kuin laillisessa ketjussa, hän voi lähettää vilpillisen ketjunsa, jonka verkon solmut tunnistavat oikeaksi ketjuksi.