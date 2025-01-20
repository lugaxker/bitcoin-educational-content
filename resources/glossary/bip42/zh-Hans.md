---
term: BIP42

---
改进 Bitcoin Core 的提案，解决了区块奖励减少计划中的一个小错误。如果不纠正这个异常现象，比特币的创造总量就会超过计划的 2100 万个上限。具体来说，在半价结束后，理论上会在 2214 年左右触发新一轮的比特币创造。出现问题的核心代码对矿工奖励的价值进行了右二进制移位操作。根据 C++ 语言标准，这一移位操作的行为是未定义的。将64位整数（`int64_t`）向右移动超过63位就属于这种未定义行为。在比特币核心代码中，这种情况可能发生在 64 个减半之后，即区块高度为 13,440,000 时。超过这个限制，位移的行为就没有定义，这意味着不同的编译可能会对代码做出不同的解释。这可能会导致不可预测的结果，包括可能造成比特币无限膨胀。BIP42 修正了这一问题，规定区块奖励在 64 个半值后设置为零，从而避免了在未定义行为的情况下使用右移操作。这一软分叉修改澄清了比特币核心代码的行为。BIP42 修正的这一错误虽然相当严重，但并不立即造成严重后果，因为它要到 2214 年左右才会显现。BIP42 于 2014 年 4 月 1 日发布，作者是 Pieter Wuille。