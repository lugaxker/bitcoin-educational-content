---
term: BIP326

---
Una propuesta de mejora dirigida a desarrolladores de software de monederos Bitcoin que soporten transacciones Taproot. Su principal objetivo es mejorar la privacidad de los protocolos de segunda capa que puedan usar PTLCs (*Contratos Bloqueados en el Tiempo*), como CoinSwap, la Lightning Network, o DLCs (*Contratos de Registro Discreto*). Para lograr esto, la propuesta busca crear una negación plausible configurando automáticamente el campo `nSequence` de las transacciones de Taproot de la misma manera que se configuró el campo `nLocktime` en otros tipos de transacciones para desalentar los ataques de francotiradores de comisiones. En otras palabras, el BIP326 pide al software de monedero que utilice el campo "nSequence" en lugar del campo "nLocktime" para evitar ataques de "fee sniping", con el fin de proporcionar una mayor privacidad para todos los protocolos fuera de la cadena que utilicen este campo de manera similar. Así, una transacción de Taproot con un valor específico en el campo `nSequence` podría ser tanto un gasto de monedero estándar como una transacción de liquidación de un protocolo de segunda capa con un bloqueo de tiempo, haciendo que estos dos casos sean indistinguibles. Si esta propuesta de mejora es ampliamente adoptada por los desarrolladores de software de monederos Bitcoin, mejoraría enormemente la privacidad y fungibilidad de Bitcoin en general.