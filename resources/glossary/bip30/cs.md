---
term: BIP30

---
Návrh na zlepšení zahrnující měkké rozvětvení zavedené 15. března 2012, které má vyřešit problém duplicitních identifikátorů transakcí. Před BIP30 bylo technicky možné mít v blockchainu dvě různé transakce se stejným identifikátorem transakce (TXID). To se stalo zejména dvakrát u transakcí s coinbase: ta v bloku 91 880 má stejný TXID jako coinbase z bloku 91 722 a ta v bloku 91 842 má stejný TXID jako coinbase z bloku 91 812. V případě transakcí s coinbase z bloku 91 880 se jednalo o dvě transakce. BIP30 tuto chybu vyřešil zavedením nového jednoduchého pravidla: žádná nová transakce nemůže mít stejné TXID jako dříve zaznamenaná transakce, pokud původní transakce nebyla zcela vyčerpána (tj. nebyly použity všechny její výstupy). Tento soft fork byl aktivován metodou flag day. Jedná se tedy o jeden z prvních UASF.