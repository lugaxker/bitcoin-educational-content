---
term: sighash_single (0x03)

---
比特币交易签名中使用的 SigHash 标志类型，表示签名适用于交易的所有输入，且只适用于一个输出，对应于同一输入签名的索引。因此，每个签名为 "SIGHASH_SINGLE "的输入都与一个特定的输出相关联。其他输出不会被签名提交，因此可以稍后修改。这种类型的签名在复杂的事务中非常有用，在这种事务中，参与者希望将某些输入链接到特定的输出，同时为事务的其他输出留有灵活性。