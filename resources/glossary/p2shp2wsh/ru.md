---
term: P2SH-P2WSH

---
P2SH-P2WSH расшифровывается как *Pay to Script Hash - Pay to Witness Script Hash*. Это стандартная модель скриптов, используемая для создания условий расходования средств на UTXO, также известная как "вложенный SegWit".

P2SH-P2WSH был представлен с внедрением SegWit в августе 2017 года. Этот скрипт описывает P2WSH, обернутый в P2SH. Он блокирует биткоины на основе хэша скрипта. Отличие от классического P2WSH заключается в том, что скрипт обернут в `redeemScript` классического P2SH.

Этот скрипт был создан во время запуска SegWit, чтобы облегчить его принятие. Он позволяет использовать этот новый стандарт даже с сервисами или кошельками, еще не совместимыми с SegWit. Сегодня использование подобных обернутых SegWit-скриптов уже неактуально, так как большинство кошельков реализовали нативный SegWit. Адреса P2SH-P2WSH записываются с использованием кодировки `Base58Check` и всегда начинаются с `3`, как и любой другой P2SH-адрес.