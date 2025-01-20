---
term: BIP61

---
在节点之间的通信协议中引入拒绝信息。BIP61 的目标是在一个节点从另一个节点收到它认为无效的交易或区块时，增加一种反馈机制。这种拒绝信息将允许节点向发送者发出信号，说明拒绝的原因。这种类型的通信旨在改善不同客户端之间的互操作性，以及完整节点与 SPV 客户端之间的通信。BIP61 带来的功能最终从 0.20.0 版本的比特币核心开始被放弃，因为这些功能被认为是不必要的，因为它们会增加带宽需求。