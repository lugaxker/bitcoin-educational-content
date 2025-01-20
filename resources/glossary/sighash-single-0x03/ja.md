---
term: sighash_single (0x03)

---
ビットコインのトランザクション署名で使用される SigHash フラグの一種で、署名がトランザクションのすべての入力に適用され、署名された同じ入力のインデックスに対応する 1 つの出力にのみ適用されることを示す。したがって、`SIGHASH_SINGLE`で署名された各入力は、特定の出力に特別にリンクされている。他の出力は署名によってコミットされないので、後で変更することができる。このタイプの署名は、トランザクションの他の出力には柔軟性を残しつつ、参加者が特定の入力を特定の出力にリンクさせたいような複雑なトランザクションで有用である。