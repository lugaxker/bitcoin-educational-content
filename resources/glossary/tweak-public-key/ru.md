---
term: ТВИК (ОТКРЫТЫЙ КЛЮЧ)

---
В области криптографии "подстройка" открытого ключа подразумевает изменение этого ключа с помощью аддитивного значения, называемого "подстройкой", таким образом, чтобы он оставался пригодным для использования при знании исходного закрытого ключа и подстройки. Технически, твик - это скалярное значение, которое добавляется к исходному открытому ключу. Если $P$ - открытый ключ, а $t$ - твик, то открытый ключ становится твиком:

$$
P' = P + tG
$$

Где $G$ - генератор используемой эллиптической кривой. Эта операция позволяет получить новый открытый ключ, производный от исходного, сохранив при этом определенные криптографические свойства, которые делают его пригодным для использования. Например, этот метод используется для адресов Taproot (P2TR), позволяя тратить средства либо путем предъявления подписи Шнорра традиционным способом, либо путем выполнения одного из условий, указанных в дереве Меркла, также называемом "MAST".

![](../../dictionnaire/assets/26.webp)