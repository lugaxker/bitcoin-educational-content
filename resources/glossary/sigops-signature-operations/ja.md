---
用語シグノプス

---
トランザクションを検証するために必要なデジタル署名操作を指す。各ビットコイン取引は複数の入力を含むことができ、それぞれが有効とみなされるために1つ以上の署名を必要とする場合がある。これらの署名の検証は、「sigops」と呼ばれる特定のオペコードを使用して行われる。具体的には、`OP_CHECKSIG`、`OP_CHECKSIGVERIFY`、`OP_CHECKMULTISIG`、`OP_CHECKMULTISIGVERIFY`がある。これらの操作は、検証を行うネットワークノードに一定の負荷を課す。人為的なsigops数の増加によるDoS攻撃を防ぐため、プロトコルはブロックごとに許可されるsigops数に制限を設け、検証負荷がノードにとって管理可能な状態に保たれるようにしている。この制限は現在、ブロックあたり最大80,000 sigopsに設定されている。カウントするために、ノードは以下のルールに従う：

scriptPubKey`では、`OP_CHECKSIG` と `OP_CHECKSIGVERIFY` は 4 シゴップとカウントされる。オペコード `OP_CHECKMULTISIG` と `OP_CHECKMULTISIGVERIFY` は 80 シゴップとカウントされる。実際、カウント中、これらのオペレーションがSegWit入力の一部でない場合、4倍される(P2WPKHの場合、sigopsの数は1になる)；

OP_CHECKMULTISIG` と `OP_CHECKMULTISIGVERIFY` は、`OP_n` の前にあれば `4n`、そうでなければ 80 シゴップとしてカウントされる；

witnessScript` では、`OP_CHECKSIG` と `OP_CHECKSIGVERIFY` は 1 シゴップ、`OP_CHECKMULTISIG` と `OP_CHECKMULTISIGVERIFY` は `OP_n` で導入されていれば `n` 、そうでなければ 20 シゴップとしてカウントされる；

Taprootスクリプトでは、sigopsの扱いが従来のスクリプトと異なります。各署名操作を直接カウントする代わりに、Taprootは各トランザクション入力にsigopsバジェットを導入し、これはその入力のサイズに比例する。このバジェットは50sigopsに入力の証人のバイトサイズを加えたものである。各署名操作はこのバジェットを50ずつ減らす。署名操作の実行によってバジェットがゼロ以下になると、スクリプトは無効となる。この方式では、シグオプスを入力のウェイトに直接リンクすることで、シグオプスに関連する潜在的な悪用からの保護を維持しながら、Taprootスクリプトの柔軟性を高めることができる。したがって、Taprootスクリプトは、ブロックあたりの80,000 sigops制限には含まれない。