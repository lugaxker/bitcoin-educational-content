---
term: overt asicboost

---
公开透明的 AsicBoost 版本。AsicBoost 是比特币挖矿中使用的一种算法优化技术。使用公开版本的矿工会操作候选区块的 `nVersion` 字段，并将此修改作为额外的 nonce。在每次散列尝试中，这种方法都会保持区块的实际 "nonce "字段不变，从而通过在每次尝试中保持一些数据不变来减少每次 SHA256 所需的计算量。与 AsicBoost 的隐蔽版本不同，该版本可被公开检测，并且不会向网络的其他部分隐藏其修改。