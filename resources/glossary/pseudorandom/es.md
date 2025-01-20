---
term: PSEUDO-RANDOM

---
Este adjetivo se utiliza para describir una secuencia de números que, a pesar de ser el resultado de un proceso determinista, presenta características próximas a las de una secuencia ideal verdaderamente aleatoria. El concepto de aleatoriedad ideal implica una ausencia total de previsibilidad y correlación entre elementos sucesivos. Un número pseudoaleatorio se genera mediante un algoritmo determinista y, por tanto, en teoría, es totalmente predecible si se conoce el estado inicial del generador.

Un generador de números pseudoaleatorios (PRNG) es un algoritmo utilizado para producir este tipo de números. Generalmente parte de un valor inicial, o "semilla", y luego aplica una serie de transformaciones matemáticas para producir la secuencia de números. Debido a esta determinabilidad, es importante para la seguridad criptográfica que la semilla inicial permanezca secreta. Las secuencias pseudoaleatorias se utilizan ampliamente en diversos campos, incluida la criptografía, ya que presentan un comportamiento aparentemente aleatorio que resulta suficiente para muchas aplicaciones. La evaluación de la calidad de un PRNG se basa en la medida en que su salida se aproxima a la aleatoriedad real en términos de distribución, correlaciones y otras propiedades estadísticas. En el contexto de Bitcoin, los números pseudoaleatorios se utilizan para producir claves privadas, o para generar una semilla para monederos deterministas y jerárquicos.