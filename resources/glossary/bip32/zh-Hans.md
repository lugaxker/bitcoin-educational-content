---
term: BIP32

---
BIP32 引入了分层确定性钱包（HD wallet）的概念。该提案允许使用单向派生函数，从一个共同的 "主种子 "生成密钥对的层次结构。每个生成的密钥对本身都可以是其他子密钥的父密钥，从而形成树状（分层）结构。BIP32 的优势在于，它可以管理多个不同的密钥对，而只需保留一个种子来重新生成它们。这一创新明显有助于解决地址重复使用的问题，而地址重复使用会严重影响用户隐私。BIP32 还允许在同一钱包内创建子分支，以方便管理。