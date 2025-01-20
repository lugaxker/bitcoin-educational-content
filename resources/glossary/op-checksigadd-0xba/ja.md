---
term: op_checksigadd (0xba)

---
スタックから `public key`, `CScriptNum` `n`, `signature` の上位 3 つの値を取り出す。署名が空のベクトルではなく、有効なものでもない場合、スクリプトはエラーで終了する。署名が有効であるか、空のベクトル (`OP_0`) である場合、2 つのシナリオが提示される：


- シグネチャが空のベクターの場合： `n` の値を持つ `CScriptNum` がスタックにプッシュされ、実行が続行される；
- シグネチャが空のベクトルでなく、有効なままであれば、`n + 1` の値を持つ `CScriptNum` がスタックにプッシュされ、実行が続行される。

単純化するために、`OP_CHECKSIGADD` は `OP_CHECKSIG` と似た操作を行いますが、スタックに true または false をプッシュする代わりに、署名が有効な場合はスタックの先頭の 2 番目の値に `1` を追加し、署名が空のベクトルを表す場合はこの値を変更せずに残します。OP_CHECKSIGADD` により、Tapscript で `OP_CHECKMULTISIG` や `OP_CHECKMULTISIGVERIFY` と同じマルチシグネチャポリシーを作成することができますが、バッチ検証可能な方法で、つまり従来のマルチシグネチャの検証におけるルックアップ処理を削除し、ノードの CPU の運用負荷を軽減しながら検証を高速化することができます。このオペコードは、TaprootのニーズのためだけにTapscriptに追加されました。