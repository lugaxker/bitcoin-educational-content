---
term: ASICBOOST

---
ASICBOOST是2016年发明的一种算法优化方法，旨在通过减少每次哈希尝试头所需的计算量，将比特币挖矿效率提高约20%。这项技术利用了用于挖矿的 SHA256 哈希函数的一个特点，即在处理数据之前将数据分成块。在多次散列尝试中，ASICBOOST 保持其中一个数据块不变，从而使矿工在多次尝试中只需完成该数据块的部分工作。这种数据共享可以重复使用以前的计算结果，从而减少找到有效哈希值所需的计算总数。

ASICBOOST 有两种使用方式：公开 ASICBOOST 和隐蔽 ASICBOOST。公开ASICBOOST形式对所有人都是可见的，因为它涉及使用区块的 "nVersion "字段作为nonce，而不改变真正的 "Nonce"。隐蔽形式试图通过使用梅克尔树来隐藏这些修改。然而，自 SegWit 推出以来，由于第二梅克尔树增加了使用该方法所需的计算量，第二种方法已变得不那么有效。

总之，ASICBOOST 允许矿工不必对所有散列尝试执行真正完整的 SHA256，因为部分结果保持不变，这加快了矿工的工作速度。