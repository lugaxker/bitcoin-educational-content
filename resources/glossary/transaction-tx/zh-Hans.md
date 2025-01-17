---
term: 交易 (tx)

---
在比特币中，交易（缩写为 "TX"）是记录在区块链上的一项操作，它将比特币的所有权从一个或多个输入转移到一个或多个输出。每笔交易都会消耗未消耗的交易输出（UTXOs）作为输入，即之前交易的输出，并创建新的UTXOs作为输出，可在未来的交易中用作输入。

每个输入都包含一个对现有输出的引用，以及一个签名脚本（`scriptSig`），该脚本满足其引用的输出所建立的消费条件（`scriptPubKey`）。这样，比特币才能解锁。输出为转移的比特币定义了新的消费条件（`scriptPubKey`），通常采用公钥或比特币现在关联的地址的形式。