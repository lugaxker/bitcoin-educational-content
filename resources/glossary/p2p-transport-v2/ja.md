---
用語P2PトランスポートV2

---
BitcoinのP2Pトランスポートプロトコルの新バージョンは、ノード間の通信のプライバシーとセキュリティを強化するために、日和見暗号化を組み込んでいる。この改良は、P2Pプロトコルの基本バージョンにおけるいくつかの問題に対処することを目的としており、特に、交換されたデータを（インターネットサービスプロバイダなどの）受動的な監視者から見分けがつかないようにすることで、データパケット内の特定のパターンを検出することによる検閲や攻撃のリスクを低減している。

実装されている暗号化には認証が含まれていないが、これは不必要な複雑さを避けるためと、ネットワーク接続のパーミッションレスな性質を損なわないためである。それにもかかわらず、この新しいP2Pトランスポート・プロトコルは、パッシブ攻撃に対してより優れたセキュリティを提供し、アクティブ攻撃（特にMITM攻撃）を大幅にコストと検出性を向上させる。擬似ランダム・データ・ストリームの導入は、通信の検閲や操作を望む攻撃者のタスクを複雑にする。

P2PトランスポートV2は、2023年12月にデプロイされたBitcoin Coreのバージョン26.0にオプション（デフォルトでは無効）として含まれている。設定ファイルの `v2transport=1` オプションで有効にできる。