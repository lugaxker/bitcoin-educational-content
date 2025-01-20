---
term: RIORGANIZZAZIONE

---
Si riferisce a un fenomeno in cui la blockchain subisce una modifica della sua struttura a causa dell'esistenza di blocchi concorrenti alla stessa altezza. Ciò si verifica quando una porzione della blockchain viene sostituita da un'altra catena che ha una maggiore quantità di lavoro accumulato.

Queste riorganizzazioni fanno parte del funzionamento naturale di Bitcoin, dove diversi minatori possono trovare nuovi blocchi quasi contemporaneamente, dividendo così la rete Bitcoin in due. In questi casi, la rete può temporaneamente dividersi in catene concorrenti. Alla fine, quando una di queste catene accumula più lavoro, le altre catene vengono abbandonate dai nodi e i loro blocchi diventano i cosiddetti "blocchi obsoleti" o "blocchi orfani" Questo processo di sostituzione di una catena con un'altra è la riorganizzazione.

![](../../dictionnaire/assets/9.webp)

Le riorganizzazioni possono avere diverse conseguenze. In primo luogo, se un utente ha avuto una transazione confermata in un blocco che si è rivelato abbandonato, ma questa transazione non compare nella catena finale valida, la sua transazione diventa nuovamente non confermata. Per questo motivo si consiglia di attendere sempre almeno 6 conferme per considerare una transazione veramente immutabile. Dopo 6 blocchi, le riorganizzazioni sono così improbabili che la possibilità che si verifichi una transazione può essere considerata praticamente nulla.

Inoltre, a livello di sistema globale, le riorganizzazioni implicano uno spreco di potenza computazionale dei minatori. Infatti, quando si verifica una divisione, alcuni minatori si troveranno sulla catena `A` e altri sulla catena `B`. Se la catena `B` viene abbandonata durante una riorganizzazione, tutta la potenza di calcolo impiegata dai minatori su questa catena è, per definizione, sprecata. Se ci sono troppe riorganizzazioni sulla rete Bitcoin, la sicurezza complessiva della rete si riduce. Questo è in parte il motivo per cui aumentare la dimensione dei blocchi o ridurre l'intervallo tra un blocco e l'altro (10 minuti) può essere pericoloso.

> *Alcuni bitcoiners preferiscono usare "blocco orfano" per riferirsi a un blocco scaduto. Inoltre, nel linguaggio comune, si usa "reorg" per indicare una "riorganizzazione" Il termine "riorganizzazione" è un anglicismo. Per essere più precisi, si potrebbe parlare di "risincronizzazione"