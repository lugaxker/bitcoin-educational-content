---
term: BLOQUE DE CANDIDATOS

---
Un bloque candidato es un bloque que está en proceso de ser creado por un minero que participa en el proceso de minería del sistema Bitcoin. El bloque candidato es una estructura de datos temporal que contiene transacciones a la espera de ser confirmadas pero que aún no tiene una prueba de trabajo válida para ser añadida al blockchain. El minero selecciona las transacciones que incluirá en el bloque candidato en función de varios factores, como las tasas de transacción asociadas y las limitaciones de tamaño del bloque. Una vez seleccionadas las transacciones, el minero genera la cabecera del bloque, que incluye la versión, un resumen de las transacciones (raíz Merkle), una marca de tiempo, el hash del bloque anterior, el objetivo de dificultad y un nonce. A continuación, el minero intenta encontrar un hash de su cabecera que cumpla el objetivo de dificultad actual. Para ello, el minero modifica el nonce presente en la cabecera. El minero también puede modificar otra información presente en su bloque candidato. Este es el mecanismo de prueba de trabajo. Si el minero consigue encontrar un hash válido, el bloque candidato se convierte en un bloque válido y se transmite a la red para ser añadido a la cadena de bloques.