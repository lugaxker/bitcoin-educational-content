---
name: Элби Хаб
description: Как легко запустить свой собственный узел Lightning?
---
![cover](assets/cover.webp)

Alby Hub - это новейшее программное обеспечение от компании Alby, создавшей популярное веб-расширение Lightning. Alby Hub - это простой в использовании интерфейс для управления узлами Lightning.

В этом руководстве мы рассмотрим различные способы использования Alby Hub для управления собственным узлом Lightning и подключения его к Alby Go, мобильному приложению Alby. Это позволит вам проводить саты в движении и быть автономным в управлении узлом.

![ALBY HUB](assets/fr/01.webp)

## Что такое Элби Хаб?

В 2024 году компания Alby отметила стратегический сдвиг. На протяжении многих лет компания предлагала различные инструменты, связанные с биткоином и Lightning Network, включая знаковое расширение Alby, которое позволяет управлять кошельком Lightning, хранилищем или иным способом. Однако в 2025 году они планируют прекратить обслуживание кошельков с общим хранилищем и сосредоточиться исключительно на решениях для самостоятельного хранения. Alby Hub станет новым флагманским инструментом в экосистеме Alby. Это программное обеспечение позволит пользователям легко управлять собственным узлом Lightning, сохраняя право собственности на свои ключи (self-custody).

Alby Hub - это легко адаптируемый инструмент. Он может удовлетворить потребности как начинающих, так и опытных пользователей. Новички будут использовать его, чтобы легко управлять реальным узлом Lightning самостоятельно, без необходимости разбираться с базовой сложностью. Для более опытных пользователей Alby Hub может использоваться как полноценный интерфейс для расширенного управления существующим узлом Lightning.

В зависимости от ваших потребностей Alby Hub доступен в 4 конфигурациях:


- Облако Элби Хаб :**

Идеальный для новичков первый вариант - облачный вариант Alby. Он позволяет развернуть узел Lightning непосредственно на управляемом Alby сервере, доступ к которому осуществляется через интерфейс Alby Hub. Хотя Alby управляет сервером, вы сохраняете суверенитет над своими средствами, поскольку ваши ключи зашифрованы с помощью пароля, известного только вам. Однако для работы узла ваши ключи должны оставаться в оперативной памяти в расшифрованном виде, что теоретически подвергает их риску, если кто-то физически получит доступ к серверу. Это интересный компромисс для новичков, но важно осознавать риски.

Основное преимущество этого варианта заключается в том, что вы получаете узел Lightning, работающий круглосуточно и без выходных, без необходимости самостоятельно управлять хостингом. Кроме того, резервное копирование узла Lightning упрощено и автоматизировано, по сравнению с вариантами с самостоятельным хостингом, где вам приходится самостоятельно управлять резервным копированием каналов.

Alby предлагает эту услугу за 21 000 сатов в месяц (тариф на декабрь 2024 года, может быть изменен, [проверьте их цены](https://albyhub.com/#pricing)). Плата автоматически списывается с вашего узла через счет-фактуру Lightning, выставляемый Alby. Это делается через соединение NWC, которое настраивает ваш узел на автоматическую оплату счетов Alby, связанных с вашей подпиской.


- Концентратор Alby с существующим узлом :**

Если у вас уже есть узел, размещенный, например, на Umbrel или Start9, Alby Hub можно использовать в качестве расширенного интерфейса управления, так же как ThunderHub или RTL.


- Элби Хаб местный :**

Можно также установить Alby Hub и узел непосредственно на ПК, хотя этот вариант менее практичен, поскольку для удаленного доступа к узлу Lightning ваш ПК должен постоянно оставаться активным. Однако этот вариант может подойти для ваших конкретных нужд.


- Alby Hub на личном сервере :**

Для опытных пользователей Alby Hub может быть развернут на персональном сервере с помощью простой команды. Этот вариант не рассматривается в данном руководстве, но вы можете найти специальные инструкции [на GitHub Alby](https://github.com/getAlby/hub?tab=readme-ov-file#docker).

Это руководство посвящено в основном интерфейсу, который будет одинаковым независимо от выбранного варианта. Мы также рассмотрим, как развернуть Alby Hub с помощью платного облачного варианта, а затем с помощью варианта "нода в коробке" (Umbrel или Start9).

![ALBY HUB](assets/fr/02.webp)

Для локальной установки на ПК [загрузите и установите программное обеспечение в соответствии с вашей операционной системой] (https://github.com/getAlby/hub/releases), затем следуйте инструкциям на интерфейсе.

![ALBY HUB](assets/fr/03.webp)

## Создайте учетную запись Alby

Первый шаг - создание учетной записи Alby. Хотя это не обязательно для использования Alby Hub, это позволит вам воспользоваться всеми доступными опциями, включая возможность получения адреса Lightning.

Зайдите на [официальный сайт Alby] (https://getalby.com/) и нажмите на кнопку "*Создать аккаунт*".

![ALBY HUB](assets/fr/04.webp)

Введите псевдоним и адрес электронной почты, затем нажмите "*Зарегистрироваться*". Этот адрес электронной почты будет использоваться для входа в вашу учетную запись в дальнейшем.

![ALBY HUB](assets/fr/05.webp)

Введите проверочный код, который вы получили по электронной почте.

![ALBY HUB](assets/fr/06.webp)

Войдя в свою учетную запись, нажмите на кнопку "*Продолжить*".

![ALBY HUB](assets/fr/07.webp)

Снова нажмите "*Продолжить*".

![ALBY HUB](assets/fr/08.webp)

## Вариант облачного хостинга

Затем вам предстоит выбрать между вариантом самостоятельного размещения, когда вы размещаете узел Lightning на собственном оборудовании, и платным вариантом с использованием облака Alby. Я начну с объяснения того, как действовать в варианте с облаком (обратите внимание, что это платный вариант, подробности см. в предыдущем разделе).

Нажмите на кнопку "*Обновить*".

![ALBY HUB](assets/fr/09.webp)

Подтвердите, нажав на кнопку "*Подписаться сейчас*".

![ALBY HUB](assets/fr/10.webp)

Нажмите на кнопку "*Запустить концентратор Alby*".

![ALBY HUB](assets/fr/11.webp)

Подождите несколько минут, пока ваш узел будет создан.

![ALBY HUB](assets/fr/12.webp)

Вот и все, теперь ваш Alby Hub настроен. В следующем разделе я покажу вам, как установить Alby Hub на существующий узел. Если вам это не нужно, вы можете перейти к следующему разделу, чтобы настроить свой узел.

![ALBY HUB](assets/fr/13.webp)

## Вариант самостоятельного хостинга

Если вы предпочитаете использовать Alby Hub в качестве интерфейса для существующего узла Lightning, у вас есть несколько вариантов: установить его на сервере, локально на вашем компьютере или с помощью узла-в-коробке (Umbrel или Start9). Использование Alby Hub в этих конфигурациях бесплатно. Мы сосредоточимся на варианте "узел-в-коробке", поскольку, на мой взгляд, серверный вариант без физического доступа сопряжен с рисками, аналогичными облачной версии, а локальная установка на ПК часто оказывается непригодной.

Чтобы настроить это на Umbrel (шаги для Start9 идентичны), у вас должен быть уже настроен узел LND.

Войдите в свой интерфейс Umbrel и перейдите в магазин приложений.

![ALBY HUB](assets/fr/14.webp)

Ищите приложение "*Alby Hub*".

![ALBY HUB](assets/fr/15.webp)

Установите его на свой узел.

![ALBY HUB](assets/fr/16.webp)

Теперь ваш интерфейс Alby Hub готов. Вы можете следовать остальной части руководства, как если бы вы использовали облачный интерфейс, но без опций платной версии. Более того, в отличие от облачной версии, ваши ключи хранятся локально на вашем узле, а не на серверах Alby.

![ALBY HUB](assets/fr/17.webp)

## Запуск хаба Алби

Нажмите на кнопку "*Начать*".

![ALBY HUB](assets/fr/18.webp)

Затем Alby Hub предложит вам выбрать пароль. Этот пароль очень важен, так как он будет использоваться для шифрования вашего кошелька. В платной облачной версии ваши ключи хранятся на сервере Alby, зашифрованы этим паролем, который знаете только вы, затем расшифрованы и хранятся только в оперативной памяти для подписания транзакций, когда это необходимо.

Поэтому очень важно выбрать надежный пароль. Любой человек с таким паролем может получить доступ к вашему узлу. Обязательно сделайте одну или несколько физических резервных копий этого пароля на листе бумаги, а еще лучше - на куске металла для дополнительной безопасности. **Если вы потеряете этот пароль, восстановить доступ к вашим биткоинам будет невозможно**, поскольку у Alby нет возможности сбросить его. Потеря этого пароля означает потерю ваших биткоинов.

После того как вы тщательно выбрали и сохранили свой пароль, нажмите на кнопку "*Создать пароль*".

![ALBY HUB](assets/fr/19.webp)

Теперь у вас есть доступ к узлу Lightning.

![ALBY HUB](assets/fr/20.webp)

Первое действие, которое необходимо предпринять, - сохранить фразу восстановления, на основе которой получены ваши ключи. Эта фраза позволит вам восстановить доступ к вашему кошельку на цепочке и, с учетом последнего состояния ваших каналов, к вашим сатам на Lightning. Для этого нажмите на "*Настройки*".

![ALBY HUB](assets/fr/21.webp)

Затем перейдите на вкладку "*Бэкап*". Введите пароль для доступа к ней.

![ALBY HUB](assets/fr/22.webp)

После этого вы получите доступ к своей фразе восстановления из 12 слов. Сделайте одну или несколько физических резервных копий этой фразы на бумаге или металле и храните их в надежном месте.

![ALBY HUB](assets/fr/23.webp)

После того как вы сохранили фразу, поставьте галочку, чтобы подтвердить ее сохранение, и нажмите "*Продолжить*".

![ALBY HUB](assets/fr/24.webp)

## Как я могу восстановить доступ к своим биткоинам?

Прежде чем отправлять средства на узел, важно понять, как вернуть их в случае возникновения проблем, а также какая информация требуется для этого. Процесс зависит от характера восстанавливаемых средств и режима хостинга вашего узла.

Для пользователей платного облака полное восстановление ваших биткоинов требует трех основных элементов:


- Ваша фраза о выздоровлении;
- Ваш пароль (тот, который используется для вашего узла) ;
- Доступ к учетной записи Alby для получения информации о состоянии ваших каналов Lightning.

Отсутствие любой из этих трех частей информации сделает невозможным полное восстановление ваших биткоинов.

Для тех, кто размещает свой собственный узел, процесс восстановления идентичен процессу восстановления любого узла Lightning. Вам потребуется :


- Ваша фраза о выздоровлении;
- Последний статус ваших каналов Lightning. Чтобы защитить эту информацию, Umbrel предлагает [опцию](https://github.com/getumbrel/umbrel/blob/2b266036f62a1594aa60a8a3be30cfb8656e755f/scripts/backup/README.md) для ее шифрования и динамического анонимного сохранения через Tor.

## Купите свой первый канал Lightning

Теперь вы можете следовать инструкциям, предоставленным Alby Hub. Нажмите на кнопку, чтобы открыть свой первый канал для поступления денежных средств.

![ALBY HUB](assets/fr/25.webp)

Выберите "*Открытый канал*". Если вы не собираетесь становиться узлом маршрутизации и не нуждаетесь в нем, я рекомендую вам выбрать закрытые каналы.

![ALBY HUB](assets/fr/26.webp)

Alby Hub сгенерирует счет для оплаты. Этот платеж покрывает транзакционные сборы, необходимые для открытия вашего канала, а также плату за услуги LSP (*Lightning Service Provider*), который откроет канал к вашему узлу, позволяя вам получать платежи немедленно.

![ALBY HUB](assets/fr/27.webp)

Как только счет будет оплачен и транзакция подтверждена, будет создан ваш первый канал Lightning.

![ALBY HUB](assets/fr/28.webp)

На вкладке "*Узел*" вы можете увидеть, что теперь у вас есть входящие деньги, что позволяет вам получать платежи через Lightning.

![ALBY HUB](assets/fr/29.webp)

Чтобы получить платеж, нажмите на вкладку "*Кошелек*", а затем на "*Получить*".

![ALBY HUB](assets/fr/30.webp)

Введите сумму и при необходимости добавьте описание, а затем нажмите "*Создать счет-фактуру*".

![ALBY HUB](assets/fr/31.webp)

Я получил свой первый платеж в размере 120 000 сатов.

![ALBY HUB](assets/fr/32.webp)

Вернувшись на вкладку "*Кошелек*", вы можете проверить баланс своего кошелька. Обратите внимание, что Alby Hub автоматически резервирует 354 сата, когда вы совершаете свой первый платеж. Для каждого канала Lightning, который вы открываете в дальнейшем, Alby Hub автоматически резервирует резерв, равный 1% от мощности канала. Этот резерв - мера безопасности, которая позволит вашей ноде вернуть средства канала в случае попытки мошенничества со стороны вашего аналога. Вот почему, хотя я отправил 120 000 сатов, на моем балансе отображается только 119 646 сатов.

![ALBY HUB](assets/fr/33.webp)

## Депозит биткоинов на цепочке

Если вы хотите иметь исходящие деньги для совершения платежей, вы также можете открыть канал самостоятельно. Для этого вам понадобятся биткоины onchain в вашем кошельке.

На вкладке "*Узел*" нажмите на "*Депозит*".

![ALBY HUB](assets/fr/34.webp)

Отправьте биткоины на отображаемый адрес. Этот адрес получен из сохраненной вами ранее фразы восстановления.

![ALBY HUB](assets/fr/35.webp)

Я отправил 72 000 сатов. Теперь они видны в разделе "*Баланс сбережений*", который включает все средства, которыми я владею на цепочке, а не на Lightning.

![ALBY HUB](assets/fr/36.webp)

## Откройте канал Lightning

Теперь, когда у вас есть средства на onchain, вы можете открыть новый канал Lightning. Рекомендуется открыть несколько каналов с достаточным количеством средств, чтобы вы всегда могли осуществлять платежи без ограничений. Большинство LSP (*Lightning Service Providers*) требуют минимум 150 000 сатов для открытия канала.

На вкладке "*Узел*" нажмите на "*Открыть канал*".

![ALBY HUB](assets/fr/37.webp)

Выберите размер вашего канала. Я рекомендую не открывать слишком маленькие каналы, учитывая, что это узел Lightning и машина, на которой хранятся ваши ключи, не обеспечивает такой же уровень безопасности, как аппаратный кошелек. Поэтому будьте осторожны с суммами, которые вы решите заблокировать.

![ALBY HUB](assets/fr/38.webp)

В меню "*Дополнительные параметры*" вы можете выбрать, с помощью какого LSP открыть канал, или вручную ввести другой узел Lightning.

![ALBY HUB](assets/fr/39.webp)

Затем нажмите на кнопку "*Открыть канал*".

![ALBY HUB](assets/fr/40.webp)

Подождите, пока ваш канал будет подтвержден на цепочке.

![ALBY HUB](assets/fr/41.webp)

Теперь ваш новый канал появится на вкладке "*Узел*".

![ALBY HUB](assets/fr/42.webp)

## Подключите приложение расходов

Теперь, когда у вас есть работающий узел Lightning, вы можете использовать его для ежедневного получения и расходования сатов. Хотя веб-интерфейс Alby Hub удобен для управления узлом, он не идеально подходит для совершения быстрых транзакций в дороге. Для этого мы будем использовать приложение Lightning-кошелька, установленное на нашем смартфоне.

В этом руководстве я рекомендую вам выбрать Alby Go, который очень прост в использовании, но вы можете использовать и другие совместимые приложения, например Zeus.

![ALBY HUB](assets/fr/43.webp)

Чтобы установить Alby Go, перейдите в магазин приложений вашего устройства:


- [Для Android](https://play.google.com/store/apps/details?id=com.getalby.mobile);
- [Для Apple] (https://apps.apple.com/us/app/alby-go/id6471335774).

![ALBY HUB](assets/fr/44.webp)

Пользователи Android также могут установить приложение через файл `.apk` [доступен на GitHub Элби] (https://github.com/getAlby/go/releases).

![ALBY HUB](assets/fr/45.webp)

Когда приложение будет запущено, нажмите на кнопку "*Подключить кошелек*".

![ALBY HUB](assets/fr/46.webp)

В центре Alby Hub на вкладке "*Подключения*" нажмите "*Добавить подключение*".

![ALBY HUB](assets/fr/47.webp)

Назовите это соединение, чтобы легко идентифицировать его в вашем хабе, и выберите разрешения, которые вы хотите предоставить приложению. В моем случае я выбрал "*Полный доступ*", чтобы иметь полный доступ к средствам узла Lightning со смартфона, но вы также можете ограничить доступ максимальным бюджетом, выбрать разрешенные функции или установить дату истечения срока действия этих разрешений. После настройки нажмите на кнопку "*Следующее*".

![ALBY HUB](assets/fr/48.webp)

После этого Alby Hub сгенерирует секрет для установления соединения.

![ALBY HUB](assets/fr/49.webp)

Вернитесь в приложение Alby Go, отсканируйте QR-код или вставьте секрет.

![ALBY HUB](assets/fr/50.webp)

Нажмите на кнопку "Готово*".

![ALBY HUB](assets/fr/51.webp)

Теперь у вас есть удаленный доступ к узлу Lightning со смартфона, что позволяет легко тратить и получать саты в пути каждый день.

![ALBY HUB](assets/fr/52.webp)

При необходимости вы можете управлять разрешениями для этого соединения прямо на Alby Hub, нажав на него.

![ALBY HUB](assets/fr/53.webp)

Чтобы получать саты, просто нажмите на кнопку "*Принять*".

![ALBY HUB](assets/fr/54.webp)

Измените сумму и описание счета, нажав на "*Счет*".

![ALBY HUB](assets/fr/55.webp)

Зарядите счет для получения сатов.

![ALBY HUB](assets/fr/56.webp)

Чтобы отправить саты, нажмите "*Отправить*".

![ALBY HUB](assets/fr/57.webp)

Отсканируйте счет, который вы хотите оплатить.

![ALBY HUB](assets/fr/58.webp)

Затем нажмите на кнопку "*Оплатить*".

![ALBY HUB](assets/fr/59.webp)

Ваша сделка подтверждена.

![ALBY HUB](assets/fr/60.webp)

Нажав на маленькую стрелку, вы можете получить доступ к истории операций.

![ALBY HUB](assets/fr/61.webp)

Эти транзакции также видны в вашем хабе Alby.

![ALBY HUB](assets/fr/62.webp)

## Настройте свой адрес Lightning

Alby предлагает вам возможность использования адреса Lightning. Это позволит вам получать платежи на свой узел без необходимости каждый раз вручную генерировать счет-фактуру. По умолчанию Alby назначает вам Lightning-адрес, но вы можете настроить его. Войдите в свою учетную запись Alby, нажмите на свое имя в правом верхнем углу, затем выберите "*Настройки*".

![ALBY HUB](assets/fr/63.webp)

Перейдите в меню "*Адрес молнии*".

![ALBY HUB](assets/fr/64.webp)

Измените свой адрес, а затем подтвердите, нажав на кнопку "*Обновить адрес молнии*".

![ALBY HUB](assets/fr/65.webp)

Обратите внимание, что после изменения адреса он больше не принадлежит вам. Поэтому убедитесь, что вы больше никогда не будете отправлять на него саты.

Вот и все, теперь вы знаете, как использовать Lightning с собственным узлом с помощью инструмента Alby Hub. Если вы нашли это руководство полезным, я буду очень благодарен, если вы поставите зеленый палец ниже. Пожалуйста, не стесняйтесь поделиться этой статьей в своих социальных сетях. Большое спасибо!

Чтобы детально разобраться во всех механизмах Lightning, которыми мы манипулировали в этом уроке, я настоятельно советую вам ознакомиться с нашим бесплатным тренингом на эту тему:

https://planb.network/courses/lnp201