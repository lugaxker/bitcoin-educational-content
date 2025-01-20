---
term: SEGWIT

---
SegWit, což je zkratka pro "Segregated Witness", je aktualizace protokolu Bitcoin představená v srpnu 2017. Jejím cílem je vyřešit několik technických problémů, včetně problému s kapacitou transakcí v síti, problému s podvržeností transakcí a usnadnění budoucích úprav protokolu.

Tento soft fork mění strukturu transakce přesunutím podpisových dat do samostatného adresáře. Konkrétně u SegWit jsou podpisy odstraněny z hlavního bloku a vloženy do samostatné datové struktury na konci bloku, známé jako svědci. Toto oddělení umožňuje zvýšit kapacitu každého bloku, aniž by se změnila maximální velikost samotného bloku, která je u Bitcoinu 1 MB. Tato změna také řeší problém s malnutelností transakcí. Před SegWitem bylo možné podpisy změnit před potvrzením transakce, čímž se změnil identifikátor transakce. To ztěžovalo sestavování složitých transakcí, protože u nepotvrzené transakce mohl být změněn její identifikátor. Oddělením podpisů SegWit znemožňuje falšování transakcí, protože jakákoli změna podpisů nyní ovlivňuje pouze identifikátor svědka (WTXID), nikoli identifikátor transakce (TXID). Vyřešením problému malleability připravil SegWit půdu pro další vývoj nad systémem Bitcoin, zejména pro Lightning Network, která umožňuje rychlé a levné transakce.