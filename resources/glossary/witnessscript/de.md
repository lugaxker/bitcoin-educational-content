---
term: WITNESSSCRIPT

---
Ein Skript, das die Bedingungen festlegt, unter denen Bitcoins von P2WSH oder P2SH-P2WSH UTXOs ausgegeben werden können. Typischerweise bestimmt `witnessScript` die Bedingungen einer Multisignatur-Wallet nach dem SegWit-Standard. Bei diesen Skript-Standards enthält der `scriptPubKey` der UTXO (die Ausgabe) einen Hash des `witnessScript`. Um diesen UTXO als Eingabe für eine neue Transaktion zu verwenden, muss der Inhaber das ursprüngliche "WitnessScript" offenlegen, um seine Übereinstimmung mit dem Fingerabdruck im "ScriptPubKey" zu beweisen. Das "WitnessScript" muss dann in das "ScriptWitness" der Transaktion aufgenommen werden, das auch die für die Validierung des Skripts erforderlichen Elemente, wie z. B. Signaturen, enthält. Daher ist das "WitnessScript" für SegWit das Äquivalent zum "RedeemScript" in einer P2SH-Transaktion, mit dem Unterschied, dass es im Zeugen der Transaktion und nicht im "ScriptSig" enthalten ist.

> ► *Achtung, das `witnessScript` ist nicht mit dem `scriptWitness` zu verwechseln. Während das `witnessScript` die Ausgabebedingungen eines P2WSH oder P2SH-P2WSH UTXO definiert und ein eigenständiges Skript darstellt, enthält das `scriptWitness` die Witness-Daten einer beliebigen SegWit-Eingabe.*