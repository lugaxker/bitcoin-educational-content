---
term: op_hash256 (0xaa)

---
通过两次使用 `SHA256`函数，从堆栈中取出顶层项目并替换为其散列值。输入用 `SHA256`散列一次，然后摘要用 `SHA256`散列第二次。这两步过程会生成 256 位指纹。