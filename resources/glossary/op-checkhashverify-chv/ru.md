---
term: OP_CHECKHASHVERIFY (CHV)

---
Новый опкод, предложенный в 2012 году в BIP17 Люком Дашджром, который предлагал те же функции, что и `OP_EVAL` или P2SH. Он должен был хэшировать конец `scriptSig`, сравнивать результат с вершиной стека и признавать транзакцию недействительной, если два хэша не совпадают. Этот опкод так и не был реализован.