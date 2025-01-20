---
term: BIP35

---
允许比特币节点公开其内存池信息（即等待确认的交易）的提案。这样，其他参与者就可以通过向节点发送特定消息，实时获取未确认交易的数据。在采用 BIP35 之前，节点只能访问已确认交易的信息。这一改进为 SPV 钱包提供了接收未确认交易信息的能力，使矿工能够避免在重启过程中错过费用高昂的交易，并为外部服务分析 mempool 信息提供了便利。