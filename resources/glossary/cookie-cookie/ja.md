---
term: クッキー（.cookie）

---
Bitcoin Core の RPC (*Remote Procedure Call*) 認証に使用されるファイル。bitcoind が起動すると、一意の認証クッキーを生成し、このファイルに保存します。RPC インターフェース経由で bitcoind と対話したいクライアントやスクリプトは、このクッキーを使って安全に認証できます。この仕組みにより、ユーザー名やパスワードを手動で管理することなく、bitcoind と外部アプリケーション（例えばウォレットソフトウェアなど）の間で安全な通信を行うことができます。.cookie` ファイルは bitcoind の再起動ごとに再生成され、シャットダウン時に削除されます。