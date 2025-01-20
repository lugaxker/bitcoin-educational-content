---
term: 地址重用

---
地址重复使用是指使用同一个接收地址来阻止多个UTXO，有时是在几个不同的交易中。比特币通常使用与唯一地址相对应的加密密钥对进行锁定。由于区块链是公开的，因此很容易看到哪些地址与多少比特币相关联。在重复使用同一地址进行多次支付的情况下，可以合理地想象所有相关联的 UTXO 都属于同一个实体。因此，地址重复使用会给用户隐私带来问题。它允许在多个交易和 UTXO 之间建立确定性联系，并使链上资金追踪永久化。中本聪在白皮书中已经提到了这个问题：

> "*作为额外的防火墙，每笔交易都可以使用一对新的密钥，以防止它们被链接到一个共同的所有者。 - Nakamoto, S. (2008)."比特币：点对点电子现金系统》。查阅 https://bitcoin.org/bitcoin.pdf。
为最大限度地保护隐私，强烈建议每个收款地址只使用一次。对于每笔新付款，最好生成一个新地址。对于变更输出，也应使用新地址。幸运的是，有了确定性和分层钱包，使用多个地址变得非常容易。与钱包相关的所有密钥对都可以很容易地从种子重新生成。这也是为什么点击 "接收 "按钮时，钱包软件总是会生成一个不同的新地址。

> ► *在英语中，它被称为 "地址重用"。