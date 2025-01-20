---
term: 主钥匙

---
在 HD（分层确定性）钱包中，主私钥是从钱包种子中提取的唯一私钥。要获得主密钥，需要将 "HMAC-SHA512 "函数应用于种子，使用 "*比特币种子*"字样作为密钥。这一操作的结果会产生一个 512 位的输出，其中前 256 位构成主密钥，其余 256 位构成主链代码。主密钥和主链代码是高清钱包树形结构中所有子私钥和公钥的起点。因此，主私钥的推导深度为 0。

![](../../dictionnaire/assets/19.webp)