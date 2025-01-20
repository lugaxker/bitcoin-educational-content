---
term: ХАУМИАНСКОЕ СОЧЛЕНЕНИЕ

---
Протокол объединения монет, использующий слепые подписи Дэвида Чаума и Tor для связи между участниками и сервером координатора. Цель Chaumian coinjoin - гарантировать участникам, что координатор не сможет украсть биткоины, а также связать вместе входы и выходы.

Для этого пользователи передают координатору свой входной адрес и криптографически заблокированный адрес приема. Этот адрес, после разблокирования, предназначен для получения биткоинов в качестве выхода из coinjoin. Координатор подписывает эти токены и возвращает их пользователям. Затем пользователи анонимно подключаются к серверу координатора с новым Tor-идентификатором и сообщают свои выходные адреса в открытом виде для построения транзакции. Координатор может убедиться, что все эти адреса приема поступают от легитимных пользователей, поскольку ранее он подписал их закрытую версию своим закрытым ключом. Однако он не может связать конкретный выходной адрес с конкретным входным пользователем. Таким образом, между входами и выходами нет никакой связи, даже с точки зрения координатора. После того как транзакция создана координатором, он отправляет ее обратно участникам, которые подписывают ее, чтобы разблокировать свой вход, после проверки того, что их выход действительно находится в этой транзакции. Участники отправляют подписи координатору. Когда все подписи собраны, координатор может транслировать транзакцию coinjoin в сеть Биткойн.

![](../../dictionnaire/assets/38.webp)

Этот метод гарантирует, что координатор не сможет ни нарушить анонимность участников, ни украсть биткоины в течение всего процесса объединения монет.

Трудно с уверенностью сказать, кто первым представил идею coinjoin в Биткойне и кому пришла в голову идея использовать слепые подписи Дэвида Чаума в этом контексте. Часто считается, что первым об этом заговорил Грегори Максвелл в [сообщении на BitcoinTalk в 2013 году] (https://bitcointalk.org/index.php?topic=279249.0):

> *"С помощью слепых подписей Чаума: Пользователи подключаются и предоставляют входные данные (и меняют адреса), а также криптографически замаскированную версию адреса, на который они хотят отправить свои приватные монеты; сервер подписывает токены и возвращает их. Пользователи снова подключаются анонимно, снимают маску со своих выходных адресов и возвращают их серверу. Сервер видит, что все выходы были подписаны им и что, следовательно, все выходы исходят от действительных участников. Позже люди снова подключаются и подписываются "*
Максвелл, Г. (2013, 22 августа). *CoinJoin: Биткойн-приватность для реального мира*. Форум BitcoinTalk. https://bitcointalk.org/index.php?topic=279249.0

Однако есть и другие более ранние упоминания, как о сигнатурах Чаума в контексте микширования, так и о коинджоинах. [В июне 2011 года Дункан Таунсенд представил на BitcoinTalk](https://bitcointalk.org/index.php?topic=12751.0) микшер, который использует подписи Чаума в способе, весьма похожем на современные чаумовские коинджоины. В той же теме есть [сообщение от hashcoin в ответ Дункану Таунсенду](https://bitcointalk.org/index.php?topic=12751.msg315793#msg315793) об улучшении его микшера. В этом сообщении как раз представлено то, что наиболее близко напоминает коинджоины. Также упоминание о подобной системе есть в [сообщении от Алекса Мизрахи в 2012 году](https://gist.github.com/killerstorm/6f843e1d3ffc38191aebca67d483bd88#file-laundry), когда он консультировал создателей Tenebrix. Сам термин "коинджойн" не был придуман Грегом Максвеллом, но произошел от идеи Питера Тодда.