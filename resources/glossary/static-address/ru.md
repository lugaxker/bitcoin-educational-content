---
term: СТАТИЧЕСКИЙ АДРЕС

---
В контексте Silent Payments обозначает уникальный идентификатор, позволяющий получать платежи без повторного использования адреса, без взаимодействия и без видимой связи на цепи между различными платежами и статическим адресом. Эта техника устраняет необходимость генерировать новые, неиспользуемые адреса получения для каждой транзакции, тем самым избегая обычного взаимодействия в Биткойне, когда получатель должен предоставить новый адрес плательщику. Это в некотором роде эквивалентно коду многоразовых платежей в контексте BIP47.

Этот адрес состоит из двух открытых ключей: $B_{\text{scan}}$ для сканирования и $B_{\text{spend}}$ для трат, объединенных для формирования статического адреса $B = B_{\text{scan}} \text{ ‖ } B_{\text{spend}}$. Получатель публикует этот адрес, что позволяет отправителям получать уникальные адреса платежей без какого-либо дальнейшего взаимодействия с получателем. Чтобы управлять несколькими различными источниками платежей, к $B_{\text{spend}}$ можно добавить метку, создав таким образом несколько помеченных статических адресов $B_1$, $B_2$ и т. д. Это позволяет разделить платежи, используя один базовый адрес, и тем самым снизить нагрузку на сканирование блокчейна. Однако все статические адреса сущности могут быть легко связаны между собой благодаря общему использованию $B_{\text{scan}}$.