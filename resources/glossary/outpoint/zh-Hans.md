---
term: 外点

---
对未用交易输出（UTXO）的唯一引用。它由两个元素组成：


- txid：创建输出的事务标识符；
- vout"：事务中输出的索引。

这两个元素的组合可精确识别UTXO。例如，如果一个事务的 "txid "为 "abc...123"，而输出索引为 "0"，则输出点将被记为：

```text
abc...123:0
```

出点用于新事务的输入（`vin`），以指示正在使用哪个 UTXO。

> ► *"外点 "一词通常与 "UTXO "同义*。