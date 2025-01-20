---
期間アカウント

---
HD (Hierarchical Deterministic) ウォレットでは、アカウントは BIP32 に従った深さ 3 の派生レイヤーを表します。各アカウントは`/0'/`（硬化派生、つまり実際には`/2^31/`または`/2 147 483 648/`）から始まる連番が振られている。よく知られている`xpubs`はこの派生深度にある。現在では、通常1つのHDウォレットで使用されるアカウントは1つだけである。しかし、元々は同じウォレット内で様々なカテゴリーを使い分けるために考えられたものである。例えば、外部タップルート(P2TR)受信アドレスの標準的な派生パスを例にとると、次のようになる：m/86'/0'/0'/0/0`とすると、アカウントインデックスは2番目の`/0'/`となる。

![](../../dictionnaire/assets/17.webp)