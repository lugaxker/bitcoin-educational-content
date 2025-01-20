---
用語BIP112

---
ビットコインスクリプト言語のオペコード `OP_CHECKSEQUENCEVERIFY` (CSV) を導入する。この操作により、ブロック数または継続時間で定義された、前のトランザクションに対する一定の遅延後にのみ有効性が有効になるトランザクションの作成が可能になる。OP_CHECKSEQUENCEVERIFY` はスタックの一番上の値を入力の `nSequence` フィールドの値と比較する。その値が大きく、他のすべての条件が満たされていれば、スクリプトは有効である。このように、`OP_CHECKSEQUENCEVERIFY`は、それを消費する入力の `nSequence` フィールドの取り得る値を制限し、この `nSequence` フィールド自体が、この入力を含むトランザクションをブロックに含めることができるタイミングを制限する。BIP112は2016年7月4日のソフトフォークでBIP68とBIP113とともに導入され、BIP9方式で初めてアクティブ化された。