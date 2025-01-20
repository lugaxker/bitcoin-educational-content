---
用語BIP49

---
BIP49は、HDウォレットでNested SegWitアドレスを生成するために使用される派生方法を紹介する、情報提供的なBIPです。提案されている導出パスはBIP43とBIP44の標準に従っており、ゴールの深さにはインデックス`49'`(hardened derivation)が付いています。例えば、P2SH-P2WPKHアカウントの最初のアドレスは、次のパスから派生する：`m/49'/0'/0'/0/0`.ネストされたSegWitスクリプトは、SegWitの立ち上げ時に、その採用を容易にするために考案されました。このスクリプトは、まだSegWitにネイティブに対応していないウォレットでも、この新しい標準を使用できるようにします。