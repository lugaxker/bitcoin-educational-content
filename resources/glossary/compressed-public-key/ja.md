---
用語圧縮公開鍵

---
公開鍵は、ビットコインを受け取って安全に保管するためにスクリプトで使用される（公開鍵の形で直接、またはアドレスとして）。生の公開鍵は楕円曲線上の点で表され、それぞれ256ビットの2つの座標（`x, y`）で構成される。したがって、生の公開鍵は512ビットであり、形式を識別するための追加バイトは含まれない。一方、圧縮公開鍵は、よりコンパクトな公開鍵表現である。これは `x` 座標と、`y` 座標のパリティ（偶数または奇数）を示す接頭辞（`02`または `03`）のみを使用する。

これを実数の分野に単純化すると、楕円曲線がx軸に対して対称であるとすると、曲線上の任意の点$P$ (`x, y`)に対して、同じ曲線上にある点$P'$ (`x, -y`)が存在する。つまり、各`x`に対して、`y`の値は正と負の2つしかありえない。例えば、ある横軸 `x` に対して、楕円曲線上には、横軸は同じだが縦軸が反対の2つの点 $P1$ と $P2$ が存在する：

![](../../dictionnaire/assets/29.webp)

曲線上の2つの可能性のある点のどちらかを選択するために、 `x` にどちらの `y` を選択するかを指定する接頭辞を付加する。この方法により、公開鍵のサイズを520ビットからわずか264ビット（接頭辞8ビット＋`x`の256ビット）に減らすことができる。この表現は公開鍵の圧縮形式として知られている。

しかし、楕円曲線暗号の文脈では、実数ではなく、次数 `p` （素数）の有限体を使っている。この文脈では、`y`の「符号」はそのパリティ、つまり`y`が偶数か奇数かで決まる。接頭辞 `0x02` は偶数の `y` を表し、`0x03` は奇数の `y` を表す。

生の公開鍵（楕円曲線上の点）を16進数で表した次の例を考えてみよう：

```plaintext
K = 04678afdb0fe5548271967f1a67130b7105cd6a828e03909a67962e0ea1f61deb649f
6bc3f4cef38c4f35504e51ec112de5c384df7ba0b8d578a4c702b6bf11d5f
```

接頭辞、`x`、`y`を分離することができる：

```plaintext
Prefix = 04
To determine the parity of `y`, we examine the last hexadecimal character of `y`:
```

ベース16（16進数）： f

10進数：15

yは奇数

```
The prefix for the compressed public key will be `03`. The compressed public key in hexadecimal becomes:
```

K = 03678afdb0fe5548271967f1a67130b7105cd6a828e03909a67962e0ea1f61deb6

```