---
term: 恢复途径

---
在使用 Miniscript 的钱包软件（例如 Liana）中，恢复路径指的是一组密钥，只有在锁定比特币的脚本（时间锁）中规定的不活动时间段后才可使用。恢复路径只有在时间锁过期后才能使用，因此提供了一种在主路径不可用时恢复资金的方法。举个例子，一个脚本包含 2 个不同的密钥：密钥 A 授权立即使用比特币，密钥 B 允许在 52,560 个区块的时间锁所定义的延迟后使用比特币。在这个例子中，密钥 A 来自主路径，而密钥 B 来自恢复路径。