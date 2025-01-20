---
用語ブロックインデックス

---
Bitcoin Core の LevelDB データ構造で、すべてのブロックに関するメタデータをカタログ化する。このインデックスの各エントリには、ブロックの識別子、ブロックチェーン内の高さ、データベース内のブロックへのポインタ、その他のメタデータなどの詳細が記載されている。このインデックスによって、メモリに保存されたブロックを素早く取り出すことができる。