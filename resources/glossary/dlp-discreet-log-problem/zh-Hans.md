---
term: DLP（离散对数问题）

---
离散对数问题（DLP）是一个数学问题，是公钥加密算法（尤其是比特币中使用的算法）安全的基础。在一个阶数为 $q$ 的循环群中，有一个生成器 $g$，如果存在一个形式为 $g^x = h$ 的等式，那么 $x$ 就被称为相对于基数 $g$ 的 $h$ 的离散对数，模数为 $q$。简单地说，就是在已知 $g$、$h$ 和 $q$ 的情况下，确定指数 $x$。因此，离散对数是有限循环群中指数的倒数。然而，对于较大的 q$ 值，离散对数问题的求解被认为在算法上很困难。利用这一特性可以确保许多加密协议的安全性，例如用于密钥交换的 Diffie-Hellman 协议。离散对数还用于椭圆曲线加密（ECC），包括椭圆曲线数字签名算法（ECDSA）。在椭圆曲线中，离散对数问题扩展为找到一个标量 $k$，使得 $k \cdot G = K$，其中 $G$ 和 $K$ 是曲线上的点，$\cdot$ 代表点乘法运算。在比特币中，标准交易使用 ECDSA 或 Schnorr 协议来锁定 UTXO。两者都依赖于离散对数计算的不可行性。