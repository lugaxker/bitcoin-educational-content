---
term: BIP112

---
Представляет опкод `OP_CHECKSEQUENCEVERIFY` (CSV) в языке Bitcoin Script. Эта операция позволяет создавать транзакции, действительность которых вступает в силу только после определенной задержки по отношению к предыдущей транзакции, заданной либо в количестве блоков, либо в продолжительности времени. `OP_CHECKSEQUENCEVERIFY` сравнивает значение на вершине стека со значением поля `nSequence` входных данных. Если оно больше и все остальные условия выполнены, то скрипт валиден. Таким образом, `OP_CHECKSEQUENCEVERIFY` ограничивает возможные значения для поля `nSequence` затрагивающего его входа, а само это поле `nSequence` ограничивает время, когда транзакция, включающая этот вход, может быть включена в блок. BIP112 был введен через мягкий форк 4 июля 2016 года, наряду с BIP68 и BIP113, впервые активированными по методу BIP9.