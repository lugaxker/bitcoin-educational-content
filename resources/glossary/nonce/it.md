---
term: NONCE

---
Nel contesto dell'informatica, il termine "nonce" si riferisce a un numero che viene utilizzato una sola volta e poi sostituito. Spesso è casuale o pseudocasuale. I nonce sono utilizzati in vari protocolli crittografici per garantire la sicurezza del processo. Ad esempio, le firme ECDSA utilizzate nel protocollo Bitcoin prevedono l'uso di un nonce. Ciò significa che questo numero deve essere nuovo per ogni firma. In caso contrario, è possibile calcolare la chiave privata utilizzata confrontando due firme che utilizzano lo stesso nonce.

I nonces sono utilizzati anche nel processo di mining di Bitcoin. I minatori incrementano questi valori modificabili all'interno dei loro blocchi candidati. Modificano il valore nonce per trovare un hash crittografico inferiore o uguale all'obiettivo di difficoltà. Questo processo richiede una notevole potenza di calcolo, in quanto comporta una ricerca esaustiva tra un gran numero di nonce possibili. Quando un minatore trova un nonce che, incluso nel suo blocco, produce un digest che soddisfa i criteri di difficoltà, il blocco viene trasmesso alla rete e il minatore vince la ricompensa.

> *Nel 2010, alcuni ricercatori hanno scoperto che la PlayStation 3 di Sony utilizzava lo stesso nonce per firmare diversi pacchetti di codice. Questo riutilizzo del nonce ha permesso agli aggressori di calcolare la chiave privata utilizzata per firmare il software. Con la chiave privata in mano, gli aggressori potevano creare firme valide per qualsiasi codice, consentendo loro di eseguire software non autorizzato, compresi giochi pirata o sistemi operativi personalizzati, direttamente sulla PS3.*
> *C'è un malinteso comune sull'origine del termine "nonce" Alcuni sostengono che rappresenti l'abbreviazione di "numero usato una sola volta" In realtà, l'origine della parola risale al XVIII secolo e deriva dall'evoluzione semantica dell'espressione inglese antica "then anes", che significava "per l'occasione"