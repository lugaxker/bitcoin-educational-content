---
term: TIMESTAMP

---
El sellado de tiempo, o "timestamping" en inglés, es un mecanismo que consiste en asociar un marcador temporal preciso a un evento, dato o mensaje. En el contexto general de los sistemas informáticos, el sellado de tiempo se utiliza para determinar el orden cronológico de las operaciones y verificar la integridad de los datos a lo largo del tiempo.

En el caso concreto de Bitcoin, las marcas de tiempo se utilizan para establecer la cronología de las transacciones y los bloques. Cada bloque de la cadena de bloques contiene una marca de tiempo que indica el momento aproximado de su creación. Satoshi Nakamoto habla incluso de un "servidor de marcas de tiempo" en su Libro Blanco, para describir lo que hoy llamaríamos "blockchain" La función del timestamping en Bitcoin es determinar la cronología de las transacciones, con el fin de determinar, sin la intervención de una autoridad central, qué transacción fue la primera. Este mecanismo permite a cada usuario verificar la no existencia de una transacción en el pasado, y evitar así que un usuario malintencionado realice un doble gasto. Este mecanismo es justificado por Satoshi Nakamoto en su Libro Blanco con la famosa frase: "*La única manera de confirmar la ausencia de una transacción es estar al tanto de todas las transacciones.*" Esta norma se establece en el tiempo Unix, que representa el total de segundos transcurridos desde el 1 de enero de 1970.

> ► *La marca de tiempo de los bloques en Bitcoin es relativamente flexible, ya que para que una marca de tiempo se considere válida, basta con que sea mayor que la mediana del tiempo de los 11 bloques precedentes (MTP) y menor que la mediana de los tiempos devueltos por los nodos (tiempo ajustado a la red) más 2 horas.*