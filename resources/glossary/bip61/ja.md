---
用語BIP61

---
ノード間の通信プロトコルに拒絶メッセージを導入。BIP61の目的は、ノードが他のノードから無効と思われるトランザクションやブロックを受信した場合に、フィードバックメカニズムを追加することである。この拒否メッセージにより、ノードは送信者に拒否された理由を知らせることができる。この種の通信は、異なるクライアント間の相互運用性と、フルノードとSPVクライアント間の通信を改善することを意図したものである。BIP61によってもたらされた機能性は、帯域幅の増加を伴う一方で不要と見なされたため、最終的にBitcoin Coreのバージョン0.20.0から放棄された。