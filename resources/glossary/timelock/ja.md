---
用語タイムロック

---
スマートコントラクトのプリミティブで、ある取引をブロックに追加するために満たさなければならない時間ベースの条件を設定することができる。ビットコインには2種類のタイムロックがある：


- 絶対タイムロックは、トランザクションがブロックに含まれなくなる正確な瞬間を指定する；
- 相対タイムロックは、前のトランザクションの受け入れからの遅延を設定する。

タイムロックはUnix時間で表した日付かブロック番号で定義できる。最後に、タイムロックはロッキングスクリプトの特定の opcode (`OP_CHECKLOCKTIMEVERIFY` または `OP_CHECKSEQUENCEVERIFY`) を使用することでトランザクションの出力に適用したり、特定のトランザクションフィールド (`nLockTime` または `nSequence`) を使用することでトランザクション全体に適用したりすることができます。