---
term: 术语： NSEQUENCE

---
比特币交易条目中的 "nSequence "字段用于表示该条目是如何被时间锁定的。最初，它的目的是允许动态替换内存池中的交易，以实现与闪电类似的支付系统覆盖。不过，随着 BIP68 引入相对时间锁定，它的用途也发生了变化。现在，"nSequence "字段可以指定交易被纳入区块前的相对延迟时间。这个延迟可以用区块数来定义，也可以用 512 秒的倍数（即实时）来定义。需要注意的是，只有当 `nVersion` 字段大于或等于 `2`时，对 `nSequence` 字段的这种新解释才有效。这种对 `nSequence` 字段的解释是在比特币共识规则的层面上。此外，在标准化规则层面，这个字段也用于发送 RBF（Replace-By-Fee）信号。如果一笔交易的 `nSequence` 小于 `0xfffffffffe`，那么它就可以通过 RBF 在遵循该政策的节点上被替换。