---
term: NSEQUÊNCIA

---
O campo `nSequence` em uma entrada de transação Bitcoin é usado para indicar como esta entrada é bloqueada pelo tempo. Originalmente, ele era destinado a permitir a substituição dinâmica de transações em mempools para permitir uma sobreposição de sistema de pagamento semelhante ao Lightning. No entanto, seu uso evoluiu com a introdução do timelock relativo através do BIP68. O campo `nSequence` pode agora especificar um atraso relativo antes que uma transação possa ser incluída num bloco. Este atraso pode ser definido em termos do número de blocos, ou como um múltiplo de 512 segundos (ou seja, tempo real). É importante notar que esta nova interpretação do campo `nSequence` só é válida se o campo `nVersion` for maior ou igual a `2`. Essa interpretação do campo `nSequence` está no nível das regras de consenso do Bitcoin. Além disso, no nível das regras de padronização, este campo também é usado para sinalizar RBF (Replace-By-Fee). Se uma transação inclui uma `nSequence` menor que `0xfffffffe`, então ela pode ser substituída via RBF em nós que seguem esta política.