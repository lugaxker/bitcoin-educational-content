---
term: DOWNLOAD INIZIALE DEL BLOCCO (IBD)

---
Si riferisce al processo con cui un nodo scarica e verifica la blockchain dal blocco Genesis e si sincronizza con gli altri nodi della rete Bitcoin. L'IBD deve essere eseguito quando si lancia un nuovo nodo completo. All'inizio di questa sincronizzazione iniziale, il nodo non ha informazioni sulle transazioni precedenti. Pertanto, scarica ogni blocco dagli altri nodi della rete, ne verifica la validità e lo aggiunge alla propria versione locale della blockchain. Vale la pena notare che l'IBD può essere lungo e richiedere molte risorse a causa delle dimensioni crescenti della blockchain e dell'insieme di UTXO. La velocità di esecuzione dipende dalle capacità di calcolo del computer che ospita il nodo, dalla sua capacità RAM, dalla velocità del dispositivo di archiviazione e dalla larghezza di banda. Per dare un'idea, se si dispone di una connessione Internet potente e il nodo è ospitato su un MacBook di ultima generazione con molta RAM, l'IBD richiederà solo poche ore. Al contrario, se si utilizza un microcomputer come un Raspberry Pi, l'IBD potrebbe richiedere una settimana o più.

> *In francese, è generalmente accettato per riferirsi direttamente a un IBD. La traduzione talvolta utilizzata è "synchronisation initiale" o "téléchargement initial des blocs "*