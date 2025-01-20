---
term: 标准化规则

---
除共识规则外，标准化规则由每个比特币节点单独采用，以定义其内存池接受的未确认交易的结构，并向其对等节点广播。因此，这些规则是由每个节点在本地配置和执行的，不同的节点可能会有所不同。它们只适用于未确认的交易。因此，只有当交易已被包含在一个有效区块中时，节点才会接受它认为非标准的交易。

我们注意到，大多数节点都保留了 Bitcoin Core 中的默认配置，从而在整个网络中形成了统一的标准化规则。虽然符合共识规则，但不遵守这些标准化规则的交易将很难在全网广播。不过，如果它到达矿工手中，仍可被包含在有效区块中。在实践中，这些被称为 "非标准 "的交易通常通过比特币点对点网络之外的外部途径直接传送给矿工。这通常是确认这类交易的唯一方式。

例如，根据共识规则，不分配任何费用的交易既是有效的，也是非标准的，因为 Bitcoin Core 对 "minRelayTxFee "参数的默认策略是 "0.00001"（单位：BTC/kB）。

> ► *"mempool规则 "一词有时也用来指标准化规则。