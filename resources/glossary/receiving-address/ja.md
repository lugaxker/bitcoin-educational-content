---
用語受信アドレス

---
ビットコインを受け取るための情報。アドレスは通常、公開鍵を `SHA256` と `RIMPEMD160` を使ってハッシュ化し、このダイジェストにメタデータを追加することで構築される。受信アドレスを構築するために使用される公開鍵は、ユーザーのウォレットの一部であり、したがってそのシードから派生する。例えば、SegWitアドレスは以下の情報で構成される：


- ビットコイン」を指定するHRP：bc`；
- セパレーター：`1`；
- 使用したSegWitのバージョン：q` または `p`；
- ペイロード：公開鍵のダイジェスト（Taprootの場合は直接公開鍵）；
- チェックサム：BCHコード。

しかし、受信アドレスは、使用するスクリプトモデルによっては、別のものを表すこともある。たとえば、P2SHアドレスはスクリプトのハッシュを使用して構築される。一方、Taprootアドレスは、ハッシュを使用せずに、調整した公開鍵を直接含む。

受信アドレスは、英数字の文字列またはQRコードで表すことができます。各アドレスは複数回使用することができるが、これは非常に推奨されない行為である。実際、一定レベルのプライバシーを維持するためには、各ビットコインアドレスを一度だけ使用することをお勧めします。自分のウォレットに入金があるたびに、新しいアドレスを生成する必要がある。アドレスはSegWit V0アドレスでは`Bech32`、SegWit V1アドレスでは`Bech32m`、レガシーアドレスでは`Base58check`でエンコードされる。技術的な観点からは、ビットコインを受け取るということは、公開鍵（したがってアドレス）に関連付けられた秘密鍵を持っているということになります。誰かがビットコインを受け取ると、送信者はその支出に関する既存の制約を更新し、受信者だけがこの力を持つことができるようにします。

![](../../dictionnaire/assets/23.webp)