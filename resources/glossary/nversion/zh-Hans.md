---
term: 版本号

---
比特币交易中的 "nVersion "字段用于指示正在使用的交易格式的版本。它允许网络区分交易格式的不同演变，并应用相应的规则。这个字段对共识规则没有影响。这意味着分配给该字段的任何值都不会导致交易失效。但是，"nVersion "字段的标准化规则目前只接受 "1 "和 "2 "的值。目前，这个字段只用于激活 `nSequence` 字段。