---
term: op_toaltstack (0x6b)

---
メインスタック (*main stack*) の先頭を取り、オルタネートスタック (*alt stack*) に移動する。このオペコードは、後でスクリプトで使用するために、一時的にデータを保存しておくために使用される。こうして移動されたアイテムはメインスタックから取り除かれる。OP_FROMALTSTACK` はそれをメインスタックの上に戻すために使用されます。