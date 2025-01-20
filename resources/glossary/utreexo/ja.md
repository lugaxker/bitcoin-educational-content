---
用語UTREEXO

---
Tadge Dryja氏によって設計された、メルクル木をベースとしたアキュムレータを使用してビットコインノードのUTXOセットをコンパクトにするプロトコル。大きな記憶領域を必要とする古典的なUTXOセットとは異なり、Utreexoはメルクル木の根だけを保存することで必要なメモリを大幅に削減する。これにより、ノードはUTXOの完全なセットを保持することなく、トランザクション入力で使用されるUTXOの存在を検証することができる。Utreexoを使用することで、各ノードはMerkleルートと呼ばれる暗号フィンガープリントのみを保持する。トランザクションが行われる際、ユーザーはUTXOと対応するMerkleパスの所有者証明を提供する。したがって、ノードはUTXOセット全体を保存することなくトランザクションを検証することができる。このメカニズムを理解するために、図を使って例を挙げてみよう：

![](../../dictionnaire/assets/15.webp)

この例では、理解を容易にするために、UTXOセットを意図的に4つのUTXOに減らしました。実際には、この行を書いている時点で、ビットコイン上にはほぼ1億4,000万個のUTXOがあると想像することが重要です。この図では、UtreexoノードはMerkle RootをRAMに保持するだけでよい。もしUTXO No.3（黒）を消費するトランザクションを受け取った場合、証明は以下の要素で構成される：


- UTXO 3；
- ハッシュ 4；
- ハッシュ1-2。

トランザクション送信者から送信されたこの情報をもとに、Utreexoノードは以下の検証を行う：


- これはUTXO 3の刻印を計算し、HASH 3を与える；
- HASH 3とHASH 4を連結する；
- インプリントを計算し、HASH3-4となる；
- HASH 3-4とHASH 1-2を連結する；
- そのインプリントを計算し、メルクル根を与える。

このプロセスによって得られたMerkleルートが、RAMに保存されているMerkleルートと同じであれば、UTXO No.3は確かにUTXOセットの一部であると確信する。

この方法は、フルノード・オペレータのRAM要件を削減する。しかし、Utreexoには、追加のプルーフによるブロック・サイズの増加や、不足するプルーフを取得するためにUtreexoノードがブリッジ・ノードに依存する可能性などの制限があります。ブリッジ・ノードは、必要な証明をUtreexoノードに提供し、完全な検証を可能にする従来のフル・ノードである。このアプローチは効率性と分散化の間の妥協点を提供し、限られたリソースのユーザーにとってトランザクション検証をより利用しやすくします。