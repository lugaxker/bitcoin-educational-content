---
用語PBKDF2

---
PBKDF2`は*Password-Based Key Derivation Function 2*の略である。派生関数を使用してパスワードから暗号鍵を作成する方法である。パスワードと暗号ソルトを入力とし、これらのデータにあらかじめ決められた関数（多くの場合 `SHA256`や`HMAC`のようなハッシュ関数）を繰り返し適用する。このプロセスを何度も繰り返し、暗号鍵を生成する。

Bitcoin のコンテキストでは、`PBKDF2` は `HMAC-SHA512` 関数と組み合わせて使用され、12 または 24 ワードの回復フレーズから決定論的かつ階層的なウォレットのシード（種）を作成する。この場合に使用される暗号ソルトは BIP39 パスフレーズであり、繰り返し回数は `2048` である。