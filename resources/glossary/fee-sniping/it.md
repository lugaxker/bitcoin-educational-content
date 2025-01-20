---
term: RITROVAMENTO DELLE TASSE

---
Uno scenario di attacco in cui i minatori cercano di riscrivere un blocco confermato di recente per rivendicare le commissioni di transazione in esso contenute, aggiungendo al contempo transazioni ad alto costo arrivate nel frattempo nella mempool. L'obiettivo finale di questo attacco per il minatore è quello di aumentare la propria redditività. Il fee sniping può diventare sempre più redditizio quando la ricompensa del blocco diminuisce e le commissioni di transazione rappresentano una parte maggiore delle entrate dei minatori. Può anche essere vantaggioso quando le commissioni contenute nel blocco precedente sono significativamente più alte di quelle del blocco successivo migliore candidato. Per semplificare, il minatore si trova di fronte a questa scelta in termini di incentivi:


- Estrarre in modo normale dopo l'ultimo blocco, con un'alta probabilità di vincere una ricompensa bassa;
- Tentare di estrarre un blocco precedente (fee sniping), con una bassa probabilità di ottenere una ricompensa elevata.

Questo attacco rappresenta un rischio per il sistema Bitcoin, poiché più minatori lo adottano, più altri minatori, inizialmente onesti, sono incentivati a fare lo stesso. Infatti, ogni volta che un nuovo minatore si unisce a quelli che tentano lo sniping delle tariffe, aumenta la probabilità che uno dei minatori che attaccano abbia successo e, in cambio, diminuisce la probabilità che uno dei minatori onesti estenda la catena. Se questo attacco venisse portato avanti in modo massiccio e prolungato nel tempo, le conferme di blocco non sarebbero più un indicatore affidabile dell'immutabilità di una transazione Bitcoin. Ciò potrebbe potenzialmente rendere il sistema inutilizzabile.

Per contrastare questo rischio, la maggior parte dei software dei portafogli compila automaticamente il campo `nLocktime` in modo da condizionare la convalida della transazione all'inclusione nell'altezza del blocco successivo. In questo modo, diventa impossibile includere la transazione in una riscrittura del blocco precedente. Se l'uso diffuso di `nLocktime` viene adottato dagli utenti di Bitcoin, riduce in modo significativo gli incentivi per il fee sniping. Anzi, incoraggia la progressione della blockchain piuttosto che la sua riscrittura, riducendo i potenziali profitti. Per le transazioni Taproot, BIP326 propone di utilizzare il campo `nSequence` in modo simile per ottenere l'effetto equivalente del campo `nLocktime` per altri tipi di transazioni. Questo uso prenderebbe due piccioni con una fava, migliorando anche la privacy dei protocolli di secondo livello che utilizzano lo stesso campo.