---
term: LIMITE DI POLVERE

---
Si riferisce alla soglia in saturazioni al di sotto della quale un UTXO è considerato "polvere" da un nodo della rete. Questa soglia fa parte delle regole di standardizzazione che possono essere modificate in modo indipendente da ciascun nodo. In Bitcoin Core, questo limite è determinato da una tariffa specifica, impostata per default a 3.000 sats per kilobyte virtuale (sats/kvB). Questo limite mira a limitare la diffusione di transazioni contenenti quantità molto piccole di bitcoin. In effetti, un UTXO qualificato come polvere implica che il suo utilizzo non è economicamente razionale: spendere questo UTXO costerebbe di più che abbandonarlo semplicemente. Se spendere polvere non è razionale, ciò suggerisce che tali spese potrebbero essere motivate solo da incentivi esterni, spesso malevoli. Questo può essere un problema se un attore malintenzionato cerca di saturare la rete con transazioni contenenti importi minimi, con l'obiettivo di aumentare il carico operativo dei nodi e potenzialmente impedire loro di elaborare altre transazioni legittime. Per fare un'analogia (anche se un po' maldestra, lo ammetto), è un po' come se qualcuno cercasse di pagare un carrello da 100 euro interamente in monete da 1 centesimo per bloccare gli altri clienti alla cassa.