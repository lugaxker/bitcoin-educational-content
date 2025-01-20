---
term: BECH32 和 BECH32M

---
Bech32 "和 "Bech32m "是两种用于接收比特币的地址编码格式。它们基于稍作修改的基数 32。它们包含一个基于 BCH（*Bose-Chaudhuri-Hocquenghem*）纠错算法的校验和。与以 "Base58check "编码的传统地址相比，"Bech32 "和 "Bech32m "地址的校验和效率更高，可以检测并自动纠正错别字。它们的格式只使用小写字母，可读性也更好。以下是这种格式的加法矩阵，以 10 为基数：

&nbsp；

| + | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |

| --- | --- | --- | --- | --- | --- | --- | --- | --- |

| 0 | q | p | z | r | y | 9 | x | 8 |

| 8 | g | f | 2 | t | v | d | w | 0 |

| 16 | s | 3 | j | n | 5 | 4 | k | h |

| 24 | c | e | 6 | m | u | a | 7 | l |

&nbsp；

Bech32 和 Bech32m 是用于表示 SegWit 地址的编码格式。Bech32 是 BIP173 在 2017 年推出的一种地址编码格式。它使用一组由数字和小写字母组成的特定字符，以减少输入错误并方便读取。Bech32 地址一般以 `bc1` 开头，表示它们是 SegWit 的原生地址。这种格式只用于 SegWit V0 地址，以及脚本 P2WPKH（支付见证公钥散列）和 P2WSH（支付见证脚本散列）。然而，Bech32 格式存在一个意想不到的小缺陷。只要地址的最后一个字符是 "p"，添加或删除其前面的任何数量的 "q "字符都不会使校验和失效。这不会影响 SegWit V0 地址 (BIP173) 的现有使用，因为它们仅限于两个定义长度。不过，这可能会影响 Bech32 编码的未来使用。Bech32m 格式只是纠正了这一错误的 Bech32 格式。它是 2020 年与 BIP350 一起推出的。Bech32m 地址也以 `bc1` 开头，但它们是专门为兼容 SegWit V1 (Taproot) 及以后的版本而设计的，脚本为 P2TR (Pay to TapRoot)。