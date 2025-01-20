---
term: 幸运

---
矿池使用的一项指标，用于衡量矿池相对于其理论预期的表现。顾名思义，它评估矿池找到区块的运气。运气的计算方法是，根据比特币当前的难度，将理论上找到一个有效区块所需的份额数与找到该区块所产生的实际份额数进行比较。份数低于预期表示运气好，而份数高于预期则表示运气差。

通过将比特币的难度与其每秒产生的份额数和每份份额的难度相关联，矿池可以计算出理论上找到一个有效区块所需的份额数。例如，假设理论上需要 10 万个份额才能找到一个区块。如果在找到一个区块之前，矿池实际生产了 20 万份，那么它的运气就是 50%：

```text
100,000 / 200,000 = 0.5 = 50%
```

反之，如果这个资金池只产生了 50,000 份，却发现了一个有效区块，那么它的运气就是 200%：

```text
100,000 / 50,000 = 2 = 200%
```

运气是一个指标，只有在区块池发现区块后才能更新，因此它是一个定期更新的静态指标。