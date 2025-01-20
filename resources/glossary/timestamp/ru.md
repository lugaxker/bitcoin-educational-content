---
term: TIMESTAMP

---
Временная метка, или "timestamp" по-английски, - это механизм, который предполагает привязку точного временного маркера к событию, данным или сообщению. В общем контексте компьютерных систем временная метка используется для определения хронологического порядка операций и проверки целостности данных во времени.

В конкретном случае с биткойном временные метки используются для определения хронологии транзакций и блоков. Каждый блок в блокчейне содержит временную метку, указывающую на приблизительный момент его создания. Сатоши Накамото даже говорит о "сервере временных меток" в своей "Белой книге", описывая то, что мы сегодня называем "блокчейном" Роль временной метки в биткойне заключается в определении хронологии транзакций, чтобы без вмешательства центрального органа определить, какая транзакция была первой. Этот механизм позволяет каждому пользователю проверить несуществование транзакции в прошлом и, таким образом, предотвратить совершение двойной траты злоумышленником. Этот механизм обоснован Сатоши Накамото в его "Белой книге" знаменитой фразой: "*Единственный способ подтвердить отсутствие транзакции - это быть в курсе всех транзакций*" Этот стандарт установлен на времени Unix, которое представляет собой общее количество секунд, прошедших с 1 января 1970 года.

> ► *Временная метка блока в Биткойне относительно гибкая: чтобы временная метка считалась действительной, она должна быть больше медианного времени 11 предыдущих блоков (MTP) и меньше медианного времени, возвращаемого узлами (время с поправкой на сеть) плюс 2 часа.*