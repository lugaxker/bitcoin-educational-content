---
term: OP_CHECKSIGADD (0XBA)

---
Извлекает из стека три верхних значения: `публичный ключ`, `CScriptNum` `n` и `подпись`. Если подпись не является пустым вектором и не действительна, скрипт завершается с ошибкой. Если же подпись действительна или является пустым вектором (`OP_0`), то возможны два сценария:


- Если сигнатурой является пустой вектор: `CScriptNum` со значением `n` выталкивается в стек, и выполнение продолжается;
- Если сигнатура не является пустым вектором и остается действительной: в стек заносится `CScriptNum` со значением `n + 1`, и выполнение продолжается.

Для упрощения, `OP_CHECKSIGADD` выполняет операцию, аналогичную `OP_CHECKSIG`, но вместо того, чтобы заносить в стек true или false, он добавляет `1` ко второму значению на вершине стека, если подпись действительна, или оставляет это значение без изменений, если подпись представляет собой пустой вектор. `OP_CHECKSIGADD` позволяет создавать в Tapscript те же политики мультиподписей, что и с помощью `OP_CHECKMULTISIG` и `OP_CHECKMULTISIGVERIFY`, но с возможностью пакетной проверки, то есть устраняет процесс поиска при проверке традиционной мультиподписи и тем самым ускоряет проверку, снижая операционную нагрузку на процессоры узлов. Этот опкод был добавлен в Tapscript исключительно для нужд Taproot.