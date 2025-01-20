---
term: OP_CHECKSIG (0XAC)

---
Проверяет достоверность подписи по заданному открытому ключу. Берет два верхних элемента из стека: подпись и открытый ключ, и оценивает, является ли подпись корректной для хэша транзакции и указанного открытого ключа. Если проверка прошла успешно, то в стек помещается значение `1` (true), иначе `0` (false). Этот опкод был модифицирован в Tapscript для проверки подписей Шнорра.