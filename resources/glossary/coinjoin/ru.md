---
term: COINJOIN

---
Coinjoin - это техника, используемая для нарушения отслеживаемости биткоинов. Она основана на совместной транзакции с одноименной структурой: транзакция coinjoin. Транзакции Coinjoin помогают улучшить защиту конфиденциальности пользователей биткоина, затрудняя анализ транзакций сторонними наблюдателями. Эта структура позволяет смешивать несколько монет в одной транзакции, что затрудняет определение связей между входными и выходными адресами.

Общая схема работы coinjoin такова: разные пользователи, желающие перемешаться, вносят определенную сумму в качестве входа в транзакцию. Эти входы выходят в виде разных выходов одной и той же суммы. В конце транзакции невозможно определить, какой выход принадлежит тому или иному пользователю. Технически нет никакой связи между входами и выходами транзакции coinjoin. Связь между каждым пользователем и каждым UTXO разорвана, точно так же, как и история каждой монеты.

![](../../dictionnaire/assets/4.webp)

Чтобы обеспечить возможность объединения монет без потери пользователем контроля над своими средствами в любой момент, транзакция сначала создается координатором, а затем передается каждому пользователю. Каждый из них подписывает транзакцию со своей стороны, убедившись, что она ему подходит, а затем все подписи добавляются к транзакции. Если пользователь или координатор попытаются украсть чужие средства, изменив выходные данные транзакции coinjoin, то подписи будут недействительными, и транзакция будет отклонена узлами. Когда запись выходных данных участников осуществляется с помощью слепых подписей Чаума, чтобы избежать связи с входными данными, это называется "чаумовским коинджоином".

Этот механизм повышает конфиденциальность транзакций, не требуя внесения изменений в протокол Биткойна. Конкретные реализации coinjoin, такие как Whirlpool, JoinMarket или Wabisabi, предлагают решения для облегчения процесса координации между участниками и повышения эффективности транзакций coinjoin. Вот пример транзакции coinjoin:

```text
323df21f0b0756f98336437aa3d2fb87e02b59f1946b714a7b09df04d429dec2
```

Трудно с уверенностью сказать, кто первым представил идею coinjoin в Биткойне и кому пришла в голову идея использовать слепые подписи Дэвида Чаума в этом контексте. Часто считается, что первым об этом заговорил Грегори Максвелл в [сообщении на BitcoinTalk в 2013 году] (https://bitcointalk.org/index.php?topic=279249.0):

Использование слепых подписей Чаума: Пользователи подключаются и предоставляют входные данные (и меняют адреса), а также криптографически замаскированную версию адреса, на который они хотят отправить свои частные монеты; сервер подписывает токены и возвращает их. Пользователи снова подключаются анонимно, снимают маску со своих выходных адресов и отправляют их обратно на сервер. Сервер видит, что все выходы были подписаны им и что, следовательно, все выходы исходят от действительных участников. Позже люди снова подключаются и подписываются.

Максвелл, Г. (2013, 22 августа). *CoinJoin: Биткойн-приватность для реального мира*. Форум BitcoinTalk. https://bitcointalk.org/index.php?topic=279249.0

Однако есть и более ранние упоминания, как о сигнатурах Чаума в контексте микширования, так и о коинджоинах. [В июне 2011 года Дункан Таунсенд представляет на BitcoinTalk](https://bitcointalk.org/index.php?topic=12751.0) микшер, который использует подписи Чаума в способе, весьма похожем на современные чаумовские коинджоины. В том же потоке есть [сообщение от hashcoin в ответ Дункану Таунсенду](https://bitcointalk.org/index.php?topic=12751.msg315793#msg315793) об улучшении его микшера. В этом сообщении представлено то, что больше всего напоминает коинджоины. Также упоминание о подобной системе есть в [сообщении от Алекса Мизрахи в 2012 году](https://gist.github.com/killerstorm/6f843e1d3ffc38191aebca67d483bd88#file-laundry), когда он консультировал создателей Tenebrix. Сам термин "коинджойн" был придуман не Грегом Максвеллом, а произошел от идеи Питера Тодда.

> ► * Термин "coinjoin" не имеет французского перевода. Некоторые биткойнеры также используют термины "mix", "mixing" или "mixage" для обозначения транзакции coinjoin. Смешивание - это скорее процесс, используемый в основе коинджоина. Кроме того, важно не путать смешивание через коинджоин с смешиванием через центрального участника, который завладевает биткоинами во время этого процесса. Это не имеет ничего общего с коинджоином, где пользователь не теряет контроль над своими биткоинами во время процесса*