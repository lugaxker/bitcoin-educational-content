---
term: АТОМНЫЙ ОБМЕН

---
Технология, позволяющая осуществлять прямой обмен криптовалютами между двумя сторонами, без необходимости доверия и без посредников. Такие обмены называют "атомарными", поскольку они могут привести только к двум результатам:


- Либо обмен проходит успешно, и оба участника фактически обменялись своими криптовалютами;
- Или же обмен не удается, и оба участника уходят со своими первоначальными криптовалютами.

Атомные свопы могут осуществляться как с одной и той же криптовалютой, в этом случае их также называют "*coinswap*", так и между разными криптовалютами. Исторически они опирались на "хэш-контракты с временной блокировкой" (HTLC) - систему временной блокировки, которая гарантирует завершение или полную отмену обмена, сохраняя тем самым целостность средств участвующих сторон. Для этого метода требовались протоколы, способные работать как с криптовалютами, так и с таймлоками. Однако в последние годы тенденция сместилась в сторону использования *подписей-адаптеров*. Преимущество этого второго подхода заключается в том, что отпадает необходимость в скриптах, а значит, снижаются эксплуатационные расходы. Другим его важным преимуществом является то, что он не требует использования одинакового хэширования для обеих частей транзакции, что позволяет избежать выявления связи между ними.