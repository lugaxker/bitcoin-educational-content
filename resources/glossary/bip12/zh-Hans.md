---
term: BIP12

---
Gavin Andresen 关于提高比特币交易脚本的灵活性和隐私性的建议。该 BIP 建议实施一个新的脚本操作码，名为 "OP_EVAL"，允许在交易验证过程中对包含在 "scriptSig "数据中的脚本进行评估。BIP12 的主要修改是允许将一个脚本包含在另一个脚本中。这种技术可以创建更复杂的条件，这些条件可以在消费时验证，而无需向向所用地址发送比特币的用户透露。BIP12 后来被更安全的提议所取代，特别是 BIP16 (P2SH)，它提供了一种不同的方法来实现与 `OP_EVAL` 相同的目标。