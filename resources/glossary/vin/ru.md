---
term: VIN

---
Определенный элемент транзакции Биткойна, который указывает источник средств, используемых для удовлетворения выходов. Каждый `vin` ссылается на неизрасходованный выход (UTXO) из предыдущей транзакции. Транзакция может содержать несколько входов, каждый из которых идентифицируется комбинацией `txid` (идентификатор исходной транзакции) и `vout` (индекс выхода в этой транзакции).

Каждый `vin` содержит следующую информацию:


- `txid`: идентификатор предыдущей транзакции, содержащей выходные данные, используемые здесь в качестве входных;
- `vout`: индекс выхода в предыдущей транзакции;
- `scriptSig` или `scriptWitness`: скрипт разблокировки, который предоставляет необходимые данные для выполнения условий, заданных `scriptPubKey` предыдущей транзакции, средства которой расходуются, обычно путем предоставления криптографической подписи;
- `nSequence`: специфическое поле, используемое для указания способа временной привязки данного входа, а также других опций, таких как RBF.