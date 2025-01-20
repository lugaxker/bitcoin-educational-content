---
term: 压缩公钥

---
脚本中使用公钥（直接以公钥的形式或作为地址）来接收比特币并确保其安全。原始公钥由椭圆曲线上的一个点表示，由两个坐标（`x, y`）组成，每个坐标 256 比特。因此，在原始格式下，公钥的长度为 512 比特，这还不包括用于识别格式的附加字节。另一方面，压缩公钥是一种更紧凑的公钥表示形式。它只使用 `x` 坐标和表示 `y` 坐标奇偶性（偶数或奇数）的前缀（`02` 或 `03`）。

如果我们将其简化为实数域，鉴于椭圆曲线相对于 x 轴对称，对于曲线上的任何一点 $P$ (`x, y`)，都存在一个同样位于这条曲线上的点 $P'$ (`x, -y`)。这意味着对于每个 `x` 而言，`y` 的值只有正负两种可能。例如，对于给定的横座标 `x`，椭圆曲线上会有两个点 $P1$ 和 $P2$，它们共享相同的横座标，但坐标相反：

![](../../dictionnaire/assets/29.webp)

要在曲线上的两个潜在点之间做出选择，需要在 `x` 中添加一个前缀，指定要选择的 `y` 。这种方法可以把公钥的大小从 520 比特减少到 264 比特（8 比特前缀 + 256 比特 `x`）。这种表示法被称为公钥的压缩形式。

然而，在椭圆曲线密码学中，我们使用的不是实数，而是阶数为 `p`（素数）的有限域。在这种情况下，"y "的 "符号 "由其奇偶性决定，即 "y "是偶数还是奇数。前缀`0x02`表示偶数`y`，`0x03`表示奇数`y`。

下面是一个十六进制原始公开密钥（椭圆曲线上的一个点）的例子：

```plaintext
K = 04678afdb0fe5548271967f1a67130b7105cd6a828e03909a67962e0ea1f61deb649f
6bc3f4cef38c4f35504e51ec112de5c384df7ba0b8d578a4c702b6bf11d5f
```

我们可以将前缀 `x` 和 `y` 分离出来：

```plaintext
Prefix = 04
To determine the parity of `y`, we examine the last hexadecimal character of `y`:
```

基数 16（十六进制）： f

基数 10（十进制）：15

y 为奇数

```
The prefix for the compressed public key will be `03`. The compressed public key in hexadecimal becomes:
```

K = 03678afdb0fe5548271967f1a67130b7105cd6a828e03909a67962e0ea1f61deb6

```