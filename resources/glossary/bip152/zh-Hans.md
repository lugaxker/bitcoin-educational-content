---
term: BIP152

---
紧凑型区块中继 "提案，旨在减少比特币网络上区块传输所需的带宽。该协议于 2016 年 11 月在 0.13.0 版本的比特币核心中采用，它允许以紧凑的方式传输区块信息，其前提是节点的内存池中已经存储了最近区块的大部分交易。BIP152 建议只发送对等节点已经知道的交易的简短标识符，并附带一些选定的交易（主要是 coinbase 交易和节点可能不知道的交易），而不是完整地传输每笔交易，这样会造成重复。节点随后可以向其同行请求任何遗漏的交易。因此，紧凑型区块中继减少了区块传播过程中的数据交换量，从而降低了带宽峰值，提高了网络的整体效率。