---
用語BIP47

---
2015年にJustus Ranvierによって提案されたこのプロトコルは、ビットコインアドレスの再利用という重大な問題を解決することを目的としている。サトシ・ナカモトはビットコイン白書の中で、ユーザーの異なる行動の分離を維持するために、各トランザクションに個別のキーペアを使用することの重要性をすでに強調していた。BIP47は、再利用可能な支払いコードの概念を導入し、ユーザーが取引ごとに新しいビットコインアドレスを手動で生成することなく、複数の支払いを受け取ることを可能にする。これらのコードは仮想識別子として機能し、ユーザーのウォレットシードから派生し、HDウォレットの派生構造のアカウントレベルに位置する。両当事者の支払いコードの組み合わせから、各当事者は相手と再度通信する必要なく、相手に属する多数のユニークなアドレスを導き出すことができる。このプロトコルの中核は、楕円曲線上で確立されたディフィー・ヘルマン鍵交換の変種であるECDHアルゴリズム（*楕円曲線ディフィー・ヘルマン*）に依存しており、これにより両当事者は一意の受信アドレスを生成するための共有秘密を確立することができる。BIP47はBitcoin Coreに追加されておらず、コミュニティから様々な評価を受けているが、Samourai WalletやSparrow Wallet上のPayNymのような実装はそれを採用し、プライバシーツールのエコシステムに完全に統合している。