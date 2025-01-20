---
term: ASSUME UTXO

---
Параметр конфигурации в ведущем клиенте Bitcoin Core, который позволяет узлу, только что инициализированному (но еще не прошедшему IBD), отложить проверку транзакций и набора UTXO до определенного моментального снимка. Концепция основана на использовании набора UTXO (списка всех существующих UTXO на данный момент времени), предоставляемого Core и считающегося точным, что позволяет узлу очень быстро синхронизироваться с цепочкой с наибольшим количеством накопленной работы. Поскольку узел пропускает длительный этап IBD, он очень быстро становится работоспособным для своего пользователя. Предположим, что UTXO делит синхронизацию (IBD) на две части:


- Сначала узел выполняет Header First Sync (проверка только заголовков) и рассматривает набор UTXO, предоставленный Core, как действительный;
- Затем, когда узел начнет работать, он проверит всю историю блоков в фоновом режиме, обновляя новый набор UTXO, который он сам проверил. Если этот новый набор UTXO не совпадает с набором, предоставленным Core, он выдаст сообщение об ошибке.

Поэтому предположим, что UTXO ускоряет подготовку нового узла Биткойна, откладывая процесс проверки транзакций, а UTXO устанавливается через обновленный снимок, предоставляемый в Core.