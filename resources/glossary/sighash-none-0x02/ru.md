---
term: SIGHASH_NONE (0X02)

---
Тип флага SigHash, используемого в подписях транзакций Биткойна, чтобы указать, что подпись применяется ко всем входам транзакции, но не к ее выходам. Использование `SIGHASH_NONE` подразумевает, что подписывающий берет на себя обязательства только по входным данным, позволяя выходным данным оставаться неопределенными или изменяемыми после подписания. Этот тип подписи полезен в тех случаях, когда подписывающий хочет уполномочить другие стороны решать, как будут распределены биткоины в транзакции.