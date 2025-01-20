---
term: BIP66

---
引入事务中签名格式的标准化。该 BIP 的提出是为了应对 OpenSSL 在不同系统中处理签名编码方式的差异。这种异质性带来了分裂区块链的风险。BIP66 使用严格的 DER 编码（*区别编码规则*）对所有交易的签名格式进行了标准化。这一改变需要软分叉。为了激活，BIP66 使用了与 BIP34 相同的机制，要求将 `nVersion` 字段增加到版本 3，并在达到 95% 的矿工阈值后拒绝所有版本 2 或更低的区块。2015年7月4日，第363725号区块越过了这一阈值。