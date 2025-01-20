---
term: BIP42

---
Ettepanek parandada Bitcoin Core'i, mis käsitleb väikest viga plokkide tasu vähendamise ajakavas. See anomaalia oleks parandamata jätmise korral viinud bitcoinide koguloomiseni, mis oleks ületanud kavandatud 21 miljoni bitcoini piiri. Täpsemalt, pärast poolitamise lõppu oleks teoreetiliselt võinud uus bitcoinide loomise tsükkel käivituda umbes aastal 2214. Kõnealune Core'i kood kasutas kaevandaja tasu väärtuse paremale binaarset nihkeoperatsiooni. Viga tulenes selle nihkeoperatsiooni kasutamisest kontekstis, kus käitumine oli C++ keele standardite kohaselt määratlemata. 64-bitise täisarvu (`int64_t`) nihutamine rohkem kui 63 bitti paremale kuulub sellesse määratlemata käitumise kategooriasse. Bitcoin Core'i koodis võis see toimuda pärast 64 poolitamist, plokikõrgusel nr 13,440,000. Pärast seda piiri ei olnud biti nihke käitumine määratletud, mis tähendab, et erinevad kompileerimissüsteemid võisid koodi erinevalt tõlgendada. See oleks võinud viia ettearvamatute tulemusteni, sealhulgas lõpmatu bitcoin-inflatsiooni tekkimise võimaluseni. BIP42 parandas selle probleemi, määrates, et plokihüvitis tuleb pärast 64 poolitamist nulliks määrata, vältides seega parempoolse nihkeoperatsiooni kasutamist ebamäärase käitumise kontekstis. See muudatus, mis oli soft fork, selgitas seega Bitcoin Core'i koodi käitumist. Kuigi see BIP42 poolt parandatud viga oli üsna tõsine, ei olnud see kohe kriitiline, sest see oleks ilmnenud alles umbes aastal 2214. 1. aprillil 2014 Pieter Wuille'i poolt avaldatud BIP42 paistab seega silma oma humoorika tooni poolest.