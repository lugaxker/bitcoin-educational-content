---
用語ウォレット・インポート・フォーマット（WIF）

---
ビットコインの秘密鍵を、異なるウォレット間でより簡単にインポートまたはエクスポートできるようにエンコードする方法。WIF は `Base58Check` エンコーディングに基づいており、バージョンに関する情報、対応する公開鍵の圧縮、タイピング時のエラー検出のためのチェックサムを含む。WIF の秘密鍵は、非圧縮鍵の場合は `5`、圧縮鍵の場合は `K` と `L` で始まり、元の秘密鍵を再構築するために必要なすべての文字を含む。WIFフォーマットは、異なるウォレットソフトウェア間で秘密鍵を転送するための標準化された手段を提供する。