---
term: SIGOPS (SIGNATUROPERATIONEN)

---
Bezieht sich auf die digitalen Signaturvorgänge, die zur Validierung von Transaktionen erforderlich sind. Jede Bitcoin-Transaktion kann mehrere Eingaben enthalten, von denen jede eine oder mehrere Signaturen erfordert, um als gültig zu gelten. Die Überprüfung dieser Signaturen erfolgt durch die Verwendung spezifischer Opcodes, die "Sigops" genannt werden. Dazu gehören insbesondere `OP_CHECKSIG`, `OP_CHECKSIGVERIFY`, `OP_CHECKMULTISIG` und `OP_CHECKMULTISIGVERIFY`. Diese Operationen verursachen eine gewisse Arbeitslast für die Netzknoten, die sie überprüfen müssen. Um DoS-Angriffe durch eine künstliche Aufblähung der Anzahl der Sigops zu verhindern, sieht das Protokoll eine Begrenzung der pro Block zulässigen Anzahl von Sigops vor, um sicherzustellen, dass die Validierungslast für die Knoten überschaubar bleibt. Diese Grenze ist derzeit auf maximal 80.000 Sigops pro Block festgelegt. Um zu zählen, befolgen die Knoten diese Regeln:

Im `scriptPubKey` zählen `OP_CHECKSIG` und `OP_CHECKSIGVERIFY` als 4 Sigops. Die Opcodes `OP_CHECKMULTISIG` und `OP_CHECKMULTISIGVERIFY` zählen für 80 Sigops. Bei der Zählung werden diese Operationen mit 4 multipliziert, wenn sie nicht Teil einer SegWit-Eingabe sind (bei einer P2WPKH beträgt die Anzahl der Sigops daher 1);

Im `redeemScript` zählen die Opcodes `OP_CHECKSIG` und `OP_CHECKSIGVERIFY` ebenfalls als 4 Sigops, `OP_CHECKMULTISIG` und `OP_CHECKMULTISIGVERIFY` werden als `4n` gezählt, wenn sie vor `OP_n` stehen, oder 80 Sigops sonst;

Für das `WitnessScript` sind `OP_CHECKSIG` und `OP_CHECKSIGVERIFY` 1 Sigop wert, `OP_CHECKMULTISIG` und `OP_CHECKMULTISIGVERIFY` werden als `n` gezählt, wenn sie durch `OP_n` eingeführt werden, oder 20 Sigops sonst;

In Taproot-Skripten werden Sigops im Vergleich zu traditionellen Skripten anders behandelt. Anstatt jede Signaturoperation direkt zu zählen, führt Taproot ein Sigops-Budget für jede Transaktionseingabe ein, das proportional zur Größe dieser Eingabe ist. Dieses Budget beträgt 50 Sigops plus die Bytegröße des Zeugen der Eingabe. Jede Signaturoperation verringert dieses Budget um 50. Wenn durch die Ausführung einer Signaturoperation das Budget unter Null sinkt, ist das Skript ungültig. Diese Methode ermöglicht mehr Flexibilität in Taproot-Skripten und bietet gleichzeitig Schutz vor potenziellem Missbrauch im Zusammenhang mit Sigops, da sie direkt mit dem Gewicht der Eingabe verknüpft ist. Taproot-Skripte werden daher nicht in die Obergrenze von 80.000 Sigops pro Block einbezogen.