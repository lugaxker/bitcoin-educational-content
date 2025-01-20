---
用語WTXID

---
SegWit で導入されたウィットネスデータを含む従来の TXID の拡張。TXIDが証人を除いた取引データのハッシュであるのに対し、WTXIDは証人を含む取引データ全体の`SHA256d`である。WTXIDはコインベースのトランザクションをルートとする別のメルクルツリーに格納される。このように分離することで、TXID のトランザクショ ンの不正性を排除することができる。