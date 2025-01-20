---
用語アウトポイント

---
未使用トランザクション出力(UTXO)への一意の参照。2つの要素で構成される：


- txid`：出力を作成したトランザクションの識別子；
- vout`: トランザクションの出力のインデックス。

これら2つの要素の組み合わせはUTXOを正確に識別する。例えば、トランザクションの `txid` が `abc...123` で、出力インデックスが `0` の場合、アウトポイントは次のように表記される：

```text
abc...123:0
```

アウトポイントは、どのUTXOが使用されているかを示すために、新しいトランザク ションのインプット（`vin`）で使用される。

> アウトポイント」は「UTXO」と同義語として使われることが多い。