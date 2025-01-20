---
term: sighash_all (0x01)

---
Bitcoin トランザクションの署名で、その署名がトランザクションのすべてのコンポーネントに適用されることを示すために使用される SigHash フラグのタイプ。SIGHASH_ALL` を使用すると、署名者はすべての入力とすべての出力をカバーする。つまり、署名後に入力も出力も無効にすることなく変更することはできない。このタイプの SigHash Flag は、トランザクションの完全な最終性と完全性を保証するため、ビットコイン取引で最も一般的である。