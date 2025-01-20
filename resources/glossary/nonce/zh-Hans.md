---
term: NONCE

---
在计算领域，"nonce "一词指的是只使用一次然后被替换的数字。它通常是随机或伪随机的。在各种加密协议中都会用到 Nonce，以确保过程的安全性。例如，比特币协议中使用的 ECDSA 签名就包含一个非ce。这意味着每次签名时，这个数字都必须是新的。如果不是这样，就可以通过比较两个使用相同 nonce 的签名来计算所使用的私钥。

Nonces 也用于比特币挖矿过程。矿工在候选区块中增加这些可修改的值。他们修改非ce值是为了找到一个低于或等于难度目标的加密哈希值。这一过程需要大量的计算能力，因为它涉及在大量可能的 nonce 中进行穷举搜索。当矿工找到的非ce包含在其区块中时，产生的摘要符合难度标准，该区块就会广播到网络，矿工就会赢得奖励。

> ► *2010年，研究人员发现索尼的PlayStation 3在签署不同的代码包时使用了相同的nonce。这种 nonce 的重复使用使得攻击者可以计算出用于签署软件的私钥。有了私钥，攻击者就可以为任何代码创建有效签名，从而可以直接在 PS3 上运行未经授权的软件，包括盗版游戏或自定义操作系统。
> ► *关于 "nonce "一词的来源，有一个常见的误解。有些人称它是 "只使用过一次的数字 "的缩写。实际上，这个词的起源可以追溯到 18 世纪，来自古英语表达 "then anes "的语义演变，意思是 "为了场合 "*。