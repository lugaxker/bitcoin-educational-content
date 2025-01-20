---
term: 深度

---
在 HD（Hierarchical Deterministic）钱包中，深度指的是从主密钥衍生出的钱包结构中密钥（公钥或私钥）、链码、扩展密钥或地址的具体级别。这种结构的每一层都可以看作是密钥树的一层，主密钥位于树根（深度 0），随后的层级定义了各种属性，如

目的（深度 1）、货币类型（深度 2）、账户（深度 3）、链类型（深度 4）和特定地址的索引（深度 5）。

![](../../dictionnaire/assets/18.webp)

要从一个深度移动到下一个深度，需要使用从一对父键到一对子键的派生过程。

> ► *有时也用 "派生下限 "一词代替深度。