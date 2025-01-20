---
term: CHAUMIANISCHE KOINJOIN

---
Ein Coinjoin-Protokoll, das David Chaums blinde Signaturen und Tor für die Kommunikation zwischen Teilnehmern und dem Server des Koordinators nutzt. Das Ziel eines Chaum'schen Coinjoin ist es, den Teilnehmern zu versichern, dass der Koordinator weder Bitcoins stehlen, noch die Ein- und Ausgänge miteinander verbinden kann.

Um dies zu erreichen, übermitteln die Nutzer dem Koordinator ihre Eingaben und eine kryptografisch verblindete Empfangsadresse. Diese Adresse ist, sobald sie entblindet ist, für den Empfang der Bitcoins als Ergebnis des Coinjoin vorgesehen. Der Koordinator signiert diese Token und gibt sie an die Nutzer zurück. Die Benutzer verbinden sich dann wieder anonym mit einer neuen Tor-Identität mit dem Server des Koordinators und geben ihre Ausgabeadressen im Klartext für die Transaktionskonstruktion preis. Der Koordinator kann überprüfen, dass alle diese Empfangsadressen von legitimen Nutzern stammen, da er ihre verblendete Version zuvor mit seinem privaten Schlüssel signiert hat. Allerdings kann er eine bestimmte Ausgangsadresse nicht mit einem bestimmten Eingangsnutzer in Verbindung bringen. Daher gibt es keine Verbindung zwischen den Eingängen und den Ausgängen, auch nicht aus der Sicht des Koordinators. Sobald der Koordinator die Transaktion erstellt hat, sendet er sie an die Teilnehmer zurück, die sie signieren, um ihren Input freizugeben, nachdem sie überprüft haben, dass ihr Output tatsächlich in dieser Transaktion enthalten ist. Die Teilnehmer senden die Unterschrift an den Koordinator. Sobald alle Unterschriften gesammelt sind, kann der Koordinator die Coinjoin-Transaktion im Bitcoin-Netzwerk veröffentlichen.

![](../../dictionnaire/assets/38.webp)

Diese Methode stellt sicher, dass der Koordinator während des gesamten Coinjoin-Prozesses weder die Anonymität der Teilnehmer gefährden noch die Bitcoins stehlen kann.

Es ist schwierig, mit Sicherheit zu bestimmen, wer zuerst die Idee des Coinjoin auf Bitcoin eingeführt hat und wer die Idee hatte, David Chaums blinde Signaturen in diesem Zusammenhang zu verwenden. Es wird oft angenommen, dass Gregory Maxwell der erste war, der dies in [einer Nachricht auf BitcoinTalk im Jahr 2013] (https://bitcointalk.org/index.php?topic=279249.0) diskutierte:

> *"Durch die Verwendung von Chaum-Blindsignaturen: Die Nutzer stellen eine Verbindung her und geben Eingaben (und ändern Adressen) sowie eine kryptografisch verblendete Version der Adresse an, an die sie ihre privaten Münzen senden möchten; der Server signiert die Token und sendet sie zurück. Der Server signiert die Token und sendet sie zurück. Die Benutzer stellen die Verbindung anonym wieder her, demaskieren ihre Ausgabeadressen und senden sie an den Server zurück. Der Server kann sehen, dass alle Ausgaben von ihm signiert wurden und dass daher alle Ausgaben von gültigen Teilnehmern stammen. Später verbinden sich die Leute erneut und signieren. "*
Maxwell, G. (2013, 22. August). *CoinJoin: Bitcoin-Privatsphäre für die reale Welt*. BitcoinTalk Forum. https://bitcointalk.org/index.php?topic=279249.0

Es gibt jedoch noch weitere frühere Erwähnungen, sowohl für Chaums Signaturen im Zusammenhang mit dem Mischen, als auch für Coinjoins. [Im Juni 2011 präsentierte Duncan Townsend auf BitcoinTalk](https://bitcointalk.org/index.php?topic=12751.0) einen Mixer, der Chaums Signaturen in einer Weise verwendet, die modernen Chaumian Coinjoins sehr ähnlich ist. Im selben Thread gibt es [eine Nachricht von hashcoin als Antwort auf Duncan Townsend](https://bitcointalk.org/index.php?topic=12751.msg315793#msg315793) zur Verbesserung seines Mixers. In dieser Nachricht wird genau dargestellt, was Coinjoins am ähnlichsten ist. Ein ähnliches System wird auch in [einer Nachricht von Alex Mizrahi aus dem Jahr 2012](https://gist.github.com/killerstorm/6f843e1d3ffc38191aebca67d483bd88#file-laundry) erwähnt, als er die Macher von Tenebrix beriet. Der Begriff "Coinjoin" selbst wurde nicht von Greg Maxwell erfunden, sondern geht auf eine Idee von Peter Todd zurück.