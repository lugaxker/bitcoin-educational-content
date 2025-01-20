---
期間再利用可能な支払コード

---
BIP47 では、再利用可能な支払いコードはビットコインウォレットから生成される静的識別子であり、通知トランザ クションと一意のアドレスの導出を可能にする。これにより、支払いのたびに新しい未使用のアドレスを手動で導出して送信することなく、プライバシーの損失につながるアドレスの再利用を回避することができる。BIP47では、再利用可能な決済コードは以下のように構築される：


- バイト0はバージョンに対応する；
- バイト1は、特定の用途の場合に情報を追加するためのビットフィールドである；
- バイト2は、公開鍵の「y」のパリティを示す；
- バイト3からバイト34までが公開鍵の「x」の値である；
- バイト35からバイト66までは、公開鍵に関連するチェーン・コードである；
- バイト67からバイト79までは、パディングはゼロである。

一般に、HRP（Human-Readable Part）がペイメントコードの先頭に、チェックサムが末尾に追加され、base58でエンコードされる。このように、ペイメントコードの構造は、拡張キーのそれとよく似ている。たとえば、私が作成したBIP47のbase58での支払いコードを以下に示す：

```text
PM8TJSBiQmNQDwTogMAbyqJe2PE2kQXjtgh88MRTxsrnHC8zpEtJ8j7Aj628oUFk8X6P5rJ7P5qD
udE4Hwq9JXSRzGcZJbdJAjM9oVQ1UKU5j2nr7VR5
```

BIP47のPayNym実装では、支払いコードをロボットの画像に関連付けられた識別子の形で表現することもできる。例えば、これは私のものである：

```text
+throbbingpond8B1
```

PayNym実装による支払いコードの使用は、現在、PCのSparrow WalletとモバイルのSamourai Walletで利用できる。