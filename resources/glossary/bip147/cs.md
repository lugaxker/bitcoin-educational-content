---
term: BIP147

---
Návrh obsažený v soft forku SegWit, jehož cílem je vyřešit vektor malleability související s fiktivním prvkem spotřebovávaným operacemi `OP_CHECKMULTISIG` a `OP_CHECKMULTISIGVERIFY`. Kvůli historické chybě off-by-one (chyba posunu jednotky) tyto 2 opcodes odstraňují ze zásobníku další prvek nad rámec své základní funkce. Aby se předešlo chybě, je proto nutné na začátek `scriptSig` povinně zařadit fiktivní hodnotu, aby bylo odstranění splněno a chyba se obešla. Tato hodnota je zbytečná, ale musí tam být, aby byl skript platný. BIP11, který zavedl standard P2MS, doporučoval uvádět jako nepotřebnou hodnotu `OP_0`. Tento standard však nebyl na úrovni pravidel konsensu vynucován, což znamená, že tam mohla být umístěna jakákoli hodnota, aniž by transakce byla neplatná. Takto `OP_CHECKMULTISIG` a `OP_CHECKMULTISIGVERIFY` obsahovaly vektor chybovosti. BIP147 zavádí nové pravidlo konsensu s názvem `NULLDUMMY`, které vyžaduje, aby tento fiktivní prvek byl prázdné pole bajtů (`OP_0`). Jakákoli jiná hodnota vede k okamžitému selhání vyhodnocení skriptu. Tato změna se týká skriptů před zavedením systému SegWit i skriptů P2WSH a vyžádala si měkké rozvětvení.