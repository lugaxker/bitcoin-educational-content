---
用語正規由来

---
HDウォレットにおける子鍵の生成プロセス。通常の派生では、親公開鍵を `HMAC-SHA512` 関数の入力として使用し、親公開鍵と親チェーンコードから子公開鍵を生成する。このプロセスでは、親公開鍵と $2^{31}$ 未満のインデックスを連結した後、 `HMAC-SHA512` を親チェーンコードに適用する。最初の256ビットが親の秘密鍵に追加されて子の秘密鍵となり、残りの256ビットが 子のチェーンコードとなる。この方法により、拡張公開鍵が子公開鍵の導出に使用できることが保証される。標準的な導出では、アカウント深度からすべての導出レベルで通常の導出が使用される。導出パスの表記において、アポストロフィ`'`のないインデックスのみが存在する場合、 通常の導出であることを示す。