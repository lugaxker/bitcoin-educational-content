---
term: UNIX 时间

---
Unix 时间或 Unix 时间戳表示自 1970 年 1 月 1 日世界协调时（UTC）午夜（Unix Epoch）起经过的秒数。该系统用于 Unix 操作系统及其衍生系统，以通用和标准化的方式标记时间。它使时钟同步和基于时间的事件管理不受时区限制。

在比特币中，它用于节点的本地时钟，因此也用于计算网络调整时间（NAT）。网络调整时间是每个节点在本地计算出的节点时间的中值，然后以此为参考来验证区块时间戳的有效性。事实上，一个区块要被节点接受，其时间戳必须在 MTP（最近 11 个已挖掘区块的过去时间中值）和网络调整时间加 2 小时之间：

```text
MTP < Valid Timestamp < (NAT + 2h)
```

Unix Time 还可用于建立基于实时而非块数的时间锁。