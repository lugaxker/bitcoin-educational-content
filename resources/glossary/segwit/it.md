---
term: SEGWIT

---
SegWit, acronimo di "Segregated Witness", è un aggiornamento del protocollo Bitcoin introdotto nell'agosto 2017. Mira a risolvere diversi problemi tecnici, tra cui il problema della capacità di transazione della rete, il problema della malleabilità delle transazioni e la facilitazione di future modifiche del protocollo.

Questo soft fork modifica la struttura delle transazioni spostando i dati delle firme in una directory separata. In particolare, con SegWit, le firme vengono rimosse dal blocco principale e inserite in una struttura di dati separata alla fine del blocco, nota come testimoni. Questa separazione consente di aumentare la capacità di ciascun blocco senza modificare la dimensione massima del blocco stesso, che in Bitcoin è di 1 MB. Questa modifica risolve anche il problema della malleabilità delle transazioni. Prima di SegWit, le firme potevano essere alterate prima della conferma di una transazione, modificando l'identificatore della transazione. Ciò rendeva difficile la costruzione di transazioni complesse, poiché una transazione non confermata poteva subire la modifica dell'identificatore. Separando le firme, SegWit rende le transazioni non malleabili, in quanto qualsiasi modifica delle firme ora influisce solo sull'identificatore del testimone (WTXID), non sull'identificatore della transazione (TXID). Risolvendo il problema della malleabilità, SegWit ha aperto la strada a ulteriori sviluppi del sistema Bitcoin, in particolare la Lightning Network, che consente transazioni veloci e a basso costo.