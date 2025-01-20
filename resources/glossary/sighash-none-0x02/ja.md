---
term: sighash_none (0x02)

---
ビットコイントランザクションの署名で使用される SigHash フラグのタイプで、署名がトランザクションのすべての入力に適用されるが、その出力には適用されないことを示す。SIGHASH_NONE`の使用は、署名者が入力に対してのみコミットすることを意味し、出力は署名後に未確定または変更可能なままであることを許可する。このタイプの署名は、署名者が取引におけるビットコインの分配方法を決定する権限を他の当事者に与えたい場合に有用である。