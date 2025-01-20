---
term: DLP (DISCREET LOG PROBLEM)

---
O Problema do Logaritmo Discreto (DLP) é um problema matemático que está na base da segurança dos algoritmos criptográficos de chave pública, nomeadamente os utilizados na Bitcoin. Num grupo cíclico de ordem $q$, com um gerador $g$, se existir uma equação da forma $g^x = h$, então $x$ é chamado o logaritmo discreto de $h$ em relação à base $g$, módulo $q$. Em termos simples, trata-se de determinar o expoente $x$ quando $g$, $h$ e $q$ são conhecidos. O logaritmo discreto é assim o inverso da exponencial num grupo cíclico finito. No entanto, para grandes valores de $q$, a resolução do problema do logaritmo discreto é considerada difícil do ponto de vista algorítmico. Esta propriedade é explorada para garantir a segurança de muitos protocolos criptográficos, como o protocolo Diffie-Hellman para troca de chaves. O logaritmo discreto é também utilizado na criptografia de curva elíptica (ECC), nomeadamente no algoritmo de assinatura digital de curva elíptica (ECDSA). No contexto das curvas elípticas, o problema do logaritmo discreto consiste em encontrar um escalar $k$ tal que $k \cdot G = K$, em que $G$ e $K$ são pontos da curva e $\cdot$ representa a operação de multiplicação de pontos. No contexto da Bitcoin, as transacções padrão utilizam o ECDSA ou o protocolo Schnorr para bloquear UTXOs. Ambos se baseiam na inviabilidade de calcular o logaritmo discreto.