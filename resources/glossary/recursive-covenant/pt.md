---
term: RECURSIVO (CONVÉNIO)

---
Um pacto recursivo na Bitcoin é um tipo de contrato inteligente que impõe condições não só na transação atual, mas também em transacções futuras que gastam os resultados desta transação. Isto permite a criação de cadeias de transacções em que cada uma deve aderir a determinadas regras definidas pela primeira na cadeia. A recursividade cria uma sequência de transacções em que cada uma herda as restrições da sua transação-mãe. Isto permitiria um controlo complexo e a longo prazo sobre a forma como as bitcoins podem ser gastas, mas também introduziria riscos relativamente à liberdade de gasto e à fungibilidade.

Em resumo, um pacto não recursivo limitar-se-ia apenas à transação que se segue imediatamente à que estabeleceu as regras. Por outro lado, um acordo recursivo tem a capacidade de impor condições específicas a uma bitcoin indefinidamente. As transacções podem seguir-se umas às outras, mas a bitcoin em questão manterá sempre as condições iniciais que lhe estão associadas. Tecnicamente, o estabelecimento de um acordo não-recursivo ocorre quando a `scriptPubKey` de um UTXO define restrições na `scriptPubKey` dos outputs de uma transação que gasta o referido UTXO. Por outro lado, o estabelecimento de um covenant recursivo ocorre quando o `scriptPubKey` de um UTXO define restrições sobre o `scriptPubKey` dos outputs de uma transação que gasta esse UTXO, e sobre todos os `scriptPubKey` que se seguirão ao gasto desse UTXO.

De uma forma mais geral, em informática, o que se designa por "recursividade" é a capacidade de uma função se chamar a si própria, criando uma espécie de ciclo.