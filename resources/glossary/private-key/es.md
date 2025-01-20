---
term: CLAVE PRIVADA

---
Una clave privada es un elemento fundamental de la criptografía asimétrica. Es un número (256 bits en el contexto de Bitcoin) que representa un secreto criptográfico. Esta clave se utiliza para firmar digitalmente transacciones y probar la propiedad de una clave pública Bitcoin (y por extensión, una dirección receptora) satisfaciendo un `scriptPubKey`. Por tanto, las claves privadas permiten gastar bitcoins desbloqueando los UTXOs asociados a la clave pública correspondiente. Las claves privadas deben mantenerse estrictamente confidenciales, ya que su divulgación podría permitir a terceros malintencionados hacerse con el control de los fondos asociados.

En el sistema Bitcoin, la clave privada está vinculada a una clave pública mediante un algoritmo de firma digital que utiliza curvas elípticas (ECDSA o Schnorr). La clave pública se deriva de la clave privada, pero lo contrario es prácticamente imposible de conseguir debido a la dificultad computacional inherente a la resolución del problema matemático subyacente (el problema del logaritmo discreto). La clave pública se utiliza generalmente para generar una dirección Bitcoin, que se utiliza para bloquear bitcoins mediante un script. En criptografía, las claves privadas suelen ser números aleatorios o pseudoaleatorios. En el contexto específico de los monederos deterministas y jerárquicos de Bitcoin, las claves privadas se derivan determinísticamente de la semilla. Las claves privadas se confunden a menudo con la semilla o con la frase de recuperación (mnemotécnica). Sin embargo, estos elementos son distintos.

> ► *En inglés, una clave privada se denomina "private key" Este término a veces se abrevia como "privkey", o "PV"