---
term: PAYJOIN

---
一种特定的比特币交易结构，通过与收款人合作，增强用户在消费过程中的隐私。Payjoin 的独特之处在于它能够生成一种乍看之下很普通的交易，但实际上是双方之间的迷你币合。为此，交易结构让收款人与实际发款人一起参与输入。这样，收款人就可以在交易中间向自己付款，从而获得报酬。例如，如果您用 10,000 萨特的UTXO 购买了一个 6,000 萨特的法棍，并且您选择了 Payjoin，您的面包师将添加属于他们的 15,000 萨特的UTXO 作为输入，除了您的 6,000 萨特之外，他们将全额取回作为输出。

Payjoin 交易有两个目的。首先，它的目的是通过在共同输入所有权启发式（CIOH）的链分析中制造一个诱饵来误导外部观察者。通常情况下，当区块链上的一笔交易有多个输入时，就会假定所有这些输入都可能属于同一个实体。因此，当分析师检查 Payjoin 交易时，他们会认为所有输入都来自同一个人。然而，这种看法是不正确的，因为收款人也与实际付款人一起参与了输入。其次，Payjoin 还在实际付款金额方面欺骗了外部观察者。通过观察交易结构，分析师可能会认为付款金额等同于其中一项产出的金额。实际上，支付金额与任何产出都不对应。它实际上是输出中收款人的UTXO 与输入中收款人的UTXO 之间的差额。因此，Payjoin 交易属于隐写术的范畴。它允许在作为诱饵的虚假交易中隐藏交易的实际金额。

![](../../dictionnaire/assets/14.webp)

> ► *Payjoin有时也被称为 "P2EP（Pay-to-End-Point）"、"Stowaway "或 "隐匿交易"。