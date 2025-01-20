---
term: UTXO SET

---
Означает совокупность всех существующих UTXO в любой момент времени. Другими словами, это большой список всех различных биткоинов, ожидающих своей траты. Если сложить суммы всех UTXO в наборе UTXO, это даст нам общую денежную массу биткоинов в обращении. Каждый узел сети Биткойн ведет свой собственный набор UTXO в режиме реального времени. Он обновляет его по мере подтверждения новых действительных блоков с входящими в них транзакциями, которые потребляют некоторые UTXO из набора UTXO, а взамен создают новые.

Этот набор UTXO хранится в каждом узле, чтобы быстро проверить, действительно ли UTXO, потраченные на транзакции, являются легитимными. Это позволяет им обнаруживать и отклонять попытки двойного расходования средств. Набор UTXO часто оказывается в центре опасений по поводу децентрализации Биткойна, поскольку его размер, естественно, очень быстро увеличивается. Поскольку часть этого набора должна храниться в оперативной памяти, чтобы проверять транзакции за разумное время, набор UTXO может постепенно сделать эксплуатацию полноценного узла слишком дорогостоящей. Набор UTXO также оказывает значительное влияние на IBD (*Initial Block Download*). Чем больше UTXO-набора может быть размещено в оперативной памяти, тем быстрее происходит IBD. В Bitcoin Core набор UTXO хранится в папке `/chainstate`.

> ► *На английский язык "UTXO set" можно перевести как "комплект UTXO".*