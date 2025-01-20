---
术语剪切节点

---
剪枝节点，英文为 "Pruned Node"，是对区块链进行剪枝的完整节点。这包括在对最老的区块进行适当验证后，逐步删除它们，只保留最新的区块。保留限制在`bitcoin.conf`文件中通过`prune=n`参数指定，其中`n`是区块所占的最大大小，单位为兆字节（MB）。如果在该参数后注明`0`，则会禁用剪枝，节点会保留整个区块链。

剪枝节点有时被视为与完整节点不同的节点类型。对于面临存储容量限制的用户来说，使用剪枝节点尤其有趣。目前，一个完整节点必须拥有近 600 GB 的存储空间才能存储区块链。剪枝节点可将所需存储空间限制在 550 MB。虽然使用的磁盘空间较少，但剪枝节点仍能保持与完整节点类似的验证和确认水平。因此，与轻节点（SPV）相比，剪枝节点能为用户提供更多信心。