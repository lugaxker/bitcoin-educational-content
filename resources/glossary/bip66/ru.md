---
term: BIP66

---
Введена стандартизация формата подписи в транзакциях. Этот BIP был предложен в ответ на расхождение в способе, которым OpenSSL обрабатывает кодировку подписи в разных системах. Такая неоднородность создавала риск раскола блокчейна. BIP66 стандартизировал формат подписи для всех транзакций, используя строгое кодирование DER (*Различительные правила кодирования*). Это изменение потребовало мягкого форка. Для его активации BIP66 использовал тот же механизм, что и BIP34, требуя увеличить поле `nVersion` до версии 3 и отвергая все блоки версии 2 или ниже по достижении порога в 95 % майнеров. Этот порог был преодолен в блоке № 363 725 4 июля 2015 года.