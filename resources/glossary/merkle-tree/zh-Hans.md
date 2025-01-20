---
学期梅克尔树

---
梅克尔树是一种加密累加器。它是一种证明给定信息在更大集合中的成员关系的方法。它是一种数据结构，便于以紧凑的格式验证信息。在比特币系统中，梅克尔树用于将一个区块的交易分组并压缩成一个单一的哈希值，称为梅克尔根（或 "*根哈希值*"）。先对每笔交易进行散列，然后将相邻的散列分级散列在一起，直到得到 Merkle 根。

![](../../dictionnaire/assets/1.webp)

这种结构可以快速验证特定交易是否包含在给定区块中，而无需分析所有交易。例如，如果我只有 Merkle Root，并且我想验证 `TX 7` 确实是该树的一部分，我只需要以下证明：


- `TX 7`；
- `HASH 8`；
- `HASH 5-6`；
- 哈希 1-2-3-4"。

有了这些信息，我就能计算出直到 Merkle Root 的中间节点。

![](../../dictionnaire/assets/2.webp)

Merkle 树主要用于只保留区块头而不保留事务的轻节点（称为 "SPV"）。这种结构在UTTREEXO 协议和 MAST Taproot 中也能找到，UTTREEXO 协议是一种允许压缩 UTXO 节点集的协议。

> ► *默克尔树是以 1979 年设计出这种结构的密码学家拉尔夫-默克尔的名字命名的。默克尔树也可称为 "散列树"。在法语中，它被称为 "Arbre de Merkle "或 "arbre de hachage"。