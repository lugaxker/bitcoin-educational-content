---
用語ブロックヘッダー

---
ブロックヘッダは、ビットコインブロックを構築する際の主要コンポーネントとして機能するデータ構造である。各ブロックはヘッダーとトランザクションのリストから構成される。ブロックヘッダには、ブロックチェーン内のブロックの整合性と妥当性を保証する重要な情報が含まれている。ブロックヘッダは80バイトのメタデータを含み、以下の要素で構成される：


- ブロックバージョン；
- 前のブロックのハッシュ；
- トランザクションのMerkleツリールート；
- ブロックのタイムスタンプ；
- 難易度の目標
- ノンス。

例えば、2023年4月15日にFoundry USAが採掘したブロック番号785,530のヘッダーを16進数で示す：

```text
00e0ff3f5ffe3b0d9247dc437e18edc19252e4517cee941752d501000000000000000000206b
de3a10826e2acb2f28fba70463601c789293d0c9c4348d7a0d06711e97c0bcb13a64b2e00517
43f09a40
```

このヘッダーを分解すると、こうなる：


- そのバージョンだ：

```text
00e0ff3f
```


- 前のハッシュ：

```text
5ffe3b0d9247dc437e18edc19252e4517cee941752d501000000000000000000
```


- メルクルの根：

```text
206bde3a10826e2acb2f28fba70463601c789293d0c9c4348d7a0d06711e97c0
```


- タイムスタンプ：

```text
bcb13a64
```


- 目標だ：

```text
b2e00517
```


- ノンス：

```text
43f09a40
```

有効であるためには、ブロックは `SHA256d` でハッシュされた後、難易度ターゲット以下のハッシュを生成するヘッダーを持たなければならない。

> 英語では "Block Header "と呼ばれます。