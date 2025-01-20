---
term: BASE58CHECK

---
base58Check" ist eine Kodierung, die im Bitcoin-System verwendet wird, um Legacy-Empfangsadressen und bestimmte andere Daten, wie z.B. erweiterte Schlüssel, in Form von menschenlesbaren Zeichenketten darzustellen. Es ist eine Variante des "Base58"-Systems, einer Positionsdarstellung der Basis 58, die entwickelt wurde, um menschliche Transkriptionsfehler zu minimieren. Es verwendet einen Satz von 58 alphanumerischen Zeichen, bestehend aus den Ziffern von "1" bis "9", Großbuchstaben von "A" bis "Z" (ohne die Buchstaben "I" und "O", um Verwechslungen mit den Ziffern "1" und "0" zu vermeiden) und Kleinbuchstaben von "a" bis "z" (ohne den Buchstaben "l", um Verwechslungen mit der Ziffer "1" zu vermeiden). base58Check" unterscheidet sich von "Base58" durch das Hinzufügen einer Prüfsumme. Sie wird durch eine reduzierte Version eines doppelten `SHA256`-Hashes der Originaldaten (`SHA256d` oder `HASH256`) am Ende der in `Base58` kodierten Daten dargestellt. Bei der Überprüfung wird die Prüfsumme neu berechnet und mit derjenigen verglichen, die während der Kodierung hinzugefügt wurde. Wenn die beiden Hashes übereinstimmen, werden die Daten als gültig betrachtet; andernfalls wird ein Korruptions- oder Transkriptionsfehler gemeldet.

Die Verwendung von `Base58Check` in Bitcoin-Adressen und -Schlüsseln bietet mehrere Vorteile. Erstens reduziert es menschliche Fehler bei der Transkription und beim Lesen, indem es mehrdeutige Zeichen vermeidet. Zweitens schützt es vor Tippfehlern, indem es Fehler durch die Prüfsumme erkennt und meldet. Drittens reduziert die kompakte Darstellung der Daten in "Base58Check" den Platzbedarf für die Speicherung und Weitergabe von Adressen und Schlüsseln. Die neuesten Empfangsadressen (nach SegWit) haben diese "Base58Check"-Kodierung zugunsten von "Bech32"- und "Bech32m"-Kodierungen aufgegeben, die eine fortgeschrittenere Prüfsumme (mit BCH-Codes) aufweisen.