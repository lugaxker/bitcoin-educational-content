---
用語BASE58CHECK（ベース58チェック

---
Base58Check`はビットコインシステムで使用されるエンコーディングで、レガシーの受信アドレスや拡張キーなどの特定のデータを人間が読める文字列の形で表現する。これは `Base58` システムの亜種であり、人間の転写ミスを最小限に抑えるために設計された 58 進数の位置表現である。1`から`9`までの数字、`A`から`Z`までの大文字（数字の`1`と`0`との混同を避けるために`I`と`O`を除く）、`a`から`z`までの小文字（数字の`1`との混同を避けるために`l`を除く）からなる58文字の英数字を使用する。Base58Check` は `Base58` と異なり、チェックサムを追加したものである。Base58Check` は `Base58` でエンコードされたデータの最後に、元のデータの二重の `SHA256` ハッシュ（`SHA256d` または `HASH256`）を縮小したものである。検証の際には、チェックサムが再計算され、エンコード時に追加されたチェックサムと比較される。2つのハッシュが一致した場合、そのデータは有効であるとみなされる。そうでない場合は、破損または転記エラーが報告される。

ビットコインのアドレスと鍵に`Base58Check`を使用すると、いくつかの利点がある。まず、あいまいな文字を避けることで、転記や読み取りにおけるヒューマンエラーを減らすことができる。第二に、チェックサムを通じてエラーを検出し報告することで、タイプミスから保護される。第三に、`Base58Check`のコンパクトなデータ表現により、アドレスとキーの保存と共有に必要なスペースが削減される。最近の受信アドレス（SegWit以降）では、この `Base58Check` エンコーディングは放棄され、より高度なチェックサム（BCHコード）を持つ `Bech32` エンコーディングと `Bech32m` エンコーディングが採用されている。