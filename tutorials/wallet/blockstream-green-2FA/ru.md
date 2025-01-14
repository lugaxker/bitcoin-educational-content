---
name: Blockstream Green - 2FA
description: Настройка мультисигмы 2/2 на Зеленом кошельке
---
![cover](assets/cover.webp)

Программный кошелек - это приложение, установленное на компьютере, смартфоне или другом подключенном к Интернету устройстве, позволяющее управлять ключами кошелька Bitcoin и обеспечивать их безопасность. В отличие от аппаратных кошельков, которые изолируют приватные ключи, "горячие" кошельки работают в среде, потенциально подверженной кибератакам, что повышает риск пиратства и кражи.

Программные кошельки следует использовать для управления разумными суммами биткоинов, особенно для повседневных транзакций. Они также могут быть интересным вариантом для людей с ограниченными биткоин-активами, для которых инвестиции в аппаратный кошелек могут показаться несоразмерными. Однако постоянная связь с Интернетом делает их менее безопасными для хранения долгосрочных сбережений или крупных средств. Для последних лучше выбрать более надежные решения, такие как аппаратные кошельки.

В этом руководстве я покажу вам, как повысить безопасность горячего кошелька с помощью опции "*2FA*" на Blockstream Green.

![GREEN 2FA MULTISIG](assets/fr/01.webp)

## Представляем блокчейн Green

Blockstream Green - это программный кошелек, доступный на мобильных и настольных компьютерах. Ранее известный как *Green Address*, этот кошелек стал проектом Blockstream после его приобретения в 2016 году.

Green - особенно простое в использовании приложение, что делает его интересным для новичков. Оно предлагает все основные функции хорошего биткойн-кошелька, включая RBF (*Replace-by-Fee*), возможность подключения через Tor, возможность подключения собственного узла, SPV (*Simple Payment Verification*), маркировку монет и управление ими.

Blockstream Green также поддерживает сеть Liquid - сайдчейн биткоина, разработанный компанией Blockstream для быстрых и конфиденциальных транзакций вне основного блокчейна. В этом руководстве мы сосредоточимся исключительно на Биткойне, но я также сделал еще одно руководство, чтобы узнать, как использовать Liquid на Green:

https://planb.network/tutorials/wallet/mobile/blockstream-green-liquid-b3e4fb82-902e-4782-ad2b-a61ab05a543a
## опция 2/2 мультисиг (2FA)

На Green вы можете создать классический "*singlesig*" горячий кошелек. Но у вас также есть возможность "*2FA multisig*", которая повышает безопасность вашего горячего кошелька, не усложняя его повседневное управление.

Итак, вы создаете кошелек с мультисигмой 2/2, что означает, что каждая транзакция будет требовать подписи двух ключей. Первый ключ, полученный из вашей мнемонической фразы из 12 или 24 слов, защищен локально с помощью PIN-кода на вашем телефоне. Вы имеете полный контроль над этим ключом. Второй ключ хранится на серверах Blockstream, и его использование для подписи требует аутентификации, которая может быть достигнута с помощью кода, полученного по электронной почте, SMS, телефонного звонка или, как мы увидим в этом руководстве, с помощью приложения для аутентификации (Authy, Google Authenticator и т. д.).

Чтобы обеспечить вашу автономность в случае отказа Blockstream (например, в случае банкротства компании или уничтожения серверов, на которых хранится второй ключ), к вашему мультисигу применяется механизм таймлока. Этот механизм превращает мультисиг 2/2 в мультисиг 1/2 примерно через год (или ровно через 51 840 блоков, но это значение можно изменить), после чего для расходования биткоинов вашему кошельку потребуется только ваш локальный ключ. Таким образом, если вы потеряете доступ к серверам Blockstream или 2FA-аутентификации, вам нужно будет подождать максимум год, чтобы иметь возможность свободно использовать свои биткоины в своем приложении, не завися от Blockstream.

![GREEN 2FA MULTISIG](assets/fr/02.webp)

Этот метод значительно повышает безопасность вашего горячего кошелька, оставляя контроль над биткоинами и облегчая их ежедневное использование. Однако для поддержания безопасности 2FA требуется регулярное обновление таймлока. Отсчет 360 дней, в течение которых ваши средства находятся под защитой 2FA, начинается с момента получения биткоинов. Если через 360 дней после получения вы не совершили ни одной операции с этими средствами, ваши биткоины будут защищены только вашим локальным ключом, без 2FA.

Это ограничение делает вариант 2FA более подходящим для портфеля расходов, где регулярные транзакции автоматически обновляют таймлок. Для долгосрочного портфеля сбережений это может быть проблематично, поскольку вам придется каждый год думать о том, чтобы провести транзакцию по замене средств для себя до истечения срока действия таймлока.

Еще один недостаток этого метода защиты заключается в том, что вам придется использовать шаблоны скриптов меньшинства. Это означает, что с точки зрения конфиденциальности все становится сложнее: очень немногие люди используют тот же тип криптовалюты, что и вы, что облегчает стороннему наблюдателю идентификацию отпечатка вашего кошелька. Более того, такие криптовалюты будут нести более высокие транзакционные издержки из-за своего большего размера.

Если вы предпочитаете не использовать опцию 2FA и просто хотите создать кошелек "*singlesig*" на Green, я приглашаю вас ознакомиться с другим руководством:

https://planb.network/tutorials/wallet/mobile/blockstream-green-liquid-b3e4fb82-902e-4782-ad2b-a61ab05a543a
## Установка и настройка программного обеспечения Blockstream Green

Первым делом, конечно же, нужно загрузить приложение Green. Перейдите в магазин приложений:

- [Для Android](https://play.google.com/store/apps/details?id=com.greenaddress.greenbits_android_wallet);
- [Для Apple] (https://apps.apple.com/us/app/green-bitcoin-wallet/id1402243590).
![GREEN 2FA MULTISIG](assets/fr/03.webp)

Пользователи Android также могут установить приложение с помощью файла `.apk` [доступен на GitHub компании Blockstream] (https://github.com/Blockstream/green_android/releases).

![GREEN 2FA MULTISIG](assets/fr/04.webp)

Запустите приложение, затем установите флажок "Я принимаю условия...*".

![GREEN 2FA MULTISIG](assets/fr/05.webp)

Когда вы открываете Green в первый раз, на главном экране не будет настроенного портфолио. В дальнейшем, если вы будете создавать или импортировать портфели, они будут появляться в этом интерфейсе. Прежде чем перейти к созданию портфеля, советую вам настроить параметры приложения под себя. Нажмите на "Настройки приложения".

![GREEN 2FA MULTISIG](assets/fr/06.webp)

Опция "*Улучшенная конфиденциальность*", доступная только на Android, повышает уровень конфиденциальности, отключая скриншоты и скрывая предварительный просмотр приложений. Кроме того, она автоматически блокирует доступ к приложениям, как только телефон заблокирован, что усложняет раскрытие данных.

![GREEN 2FA MULTISIG](assets/fr/07.webp)

Для тех, кто хочет повысить уровень конфиденциальности, в приложении предусмотрена возможность маршрутизации трафика через Tor - сеть, которая шифрует все ваши соединения и делает вашу деятельность трудноотслеживаемой. Хотя эта опция может несколько замедлить работу приложения, она настоятельно рекомендуется для защиты вашей конфиденциальности, особенно если вы не используете свой собственный узел.

![GREEN 2FA MULTISIG](assets/fr/08.webp)

Для пользователей, имеющих собственный полноценный узел, Green Wallet предлагает возможность подключения к нему через сервер Electrum, гарантируя полный контроль над информацией о сети Bitcoin и распределением транзакций.

![GREEN 2FA MULTISIG](assets/fr/09.webp)

Другой альтернативной функцией является опция "*SPV Verification*", которая позволяет напрямую проверить определенные данные блокчейна и тем самым уменьшить необходимость доверять узлу Blockstream по умолчанию, хотя этот метод не обеспечивает всех гарантий полноценного узла.

![GREEN 2FA MULTISIG](assets/fr/10.webp)

После того как вы настроите эти параметры в соответствии с вашими потребностями, нажмите на кнопку "*Сохранить*" и перезапустите приложение.

![GREEN 2FA MULTISIG](assets/fr/11.webp)

## Создайте кошелек Bitcoin на Blockstream Green

Теперь вы готовы к созданию кошелька Bitcoin. Нажмите на кнопку "*Начать*".

![GREEN 2FA MULTISIG](assets/fr/12.webp)

Вы можете выбрать между созданием локального программного кошелька и управлением холодным кошельком через аппаратный кошелек. В этом руководстве мы сосредоточимся на создании горячего кошелька, поэтому вам нужно будет выбрать опцию "*На этом устройстве*".

![GREEN 2FA MULTISIG](assets/fr/13.webp)

Затем вы можете выбрать восстановление существующего кошелька Bitcoin или создание нового. В рамках данного руководства мы будем создавать новый кошелек. Однако если вам нужно восстановить существующий кошелек Bitcoin из его мнемонической фразы, например после потери старого телефона, вам нужно будет выбрать второй вариант.

![GREEN 2FA MULTISIG](assets/fr/14.webp)

Затем вы можете выбрать мнемоническую фразу из 12 или 24 слов. Эта фраза позволит вам восстановить доступ к кошельку с помощью любого совместимого программного обеспечения в случае проблем с телефоном. В настоящее время выбор фразы из 24 слов не обеспечивает большей безопасности, чем фраза из 12 слов. Поэтому я рекомендую вам выбрать мнемоническую фразу из 12 слов.

После этого Грин сообщит вам мнемоническую фразу. Прежде чем продолжить, убедитесь, что за вами не наблюдают. Нажмите на кнопку "*Показать фразу восстановления*", чтобы вывести ее на экран.

![GREEN 2FA MULTISIG](assets/fr/15.webp)

**Эта мнемоника дает вам полный, неограниченный доступ ко всем вашим биткоинам**. Любой человек, владеющий этой фразой, может украсть ваши средства, даже не имея физического доступа к вашему телефону (при условии просроченной блокировки по времени или 2FA в случае кошелька 2/2 на Green).

Она позволяет восстановить доступ к локальным ключам в случае потери, кражи или поломки телефона. Поэтому очень важно тщательно создать резервную копию **на физическом носителе (не цифровом)** и хранить ее в надежном месте. Вы можете записать ее на листе бумаги, а для дополнительной безопасности, если речь идет о большом кошельке, я рекомендую выгравировать ее на подставке из нержавеющей стали, чтобы защитить ее от риска пожара, наводнения или обрушения (для горячего кошелька, предназначенного для хранения небольшого количества биткоинов, вероятно, будет достаточно простой бумажной резервной копии).

*Разумеется, вы никогда не должны делиться этими словами в Интернете, как это делаю я в этом учебнике. Этот образец портфолио будет использоваться только в Testnet и будет удален по окончании урока.*

![GREEN 2FA MULTISIG](assets/fr/16.webp)

После того как вы правильно записали свою мнемоническую фразу на физический носитель, нажмите "*Продолжить*". Затем Green Wallet попросит вас подтвердить некоторые слова в вашей мнемонической фразе, чтобы убедиться, что вы записали их правильно. Заполните пропуски недостающими словами.

![GREEN 2FA MULTISIG](assets/fr/17.webp)

Выберите PIN-код вашего устройства, который будет использоваться для разблокировки Green wallet. Это ваша защита от несанкционированного физического доступа. Этот PIN-код не участвует в создании криптографических ключей вашего кошелька. Поэтому, даже не имея доступа к этому PIN-коду, владение мнемонической фразой из 12 или 24 слов позволит вам восстановить доступ к локальным ключам.

Мы рекомендуем выбрать 6-значный PIN-код, который должен быть как можно более случайным. Обязательно сохраните этот код, чтобы не забыть его, иначе вам придется восстанавливать кошелек по мнемонике. Вы можете добавить опцию биометрической блокировки, чтобы не вводить PIN-код при каждом использовании. Вообще говоря, биометрические данные гораздо менее безопасны, чем сам PIN-код. Поэтому по умолчанию я не советую устанавливать эту опцию разблокировки.

![GREEN 2FA MULTISIG](assets/fr/18.webp)

Введите PIN-код второй раз, чтобы подтвердить его.

![GREEN 2FA MULTISIG](assets/fr/19.webp)

Дождитесь создания портфолио, затем нажмите на кнопку "*Создать учетную запись*".

![GREEN 2FA MULTISIG](assets/fr/20.webp)

Затем вы можете выбрать между стандартным кошельком с одной подписью и кошельком, защищенным двухфакторной аутентификацией (2FA). В этом руководстве мы выберем второй вариант.

![GREEN 2FA MULTISIG](assets/fr/21.webp)

Ваш мультисигмальный кошелек Bitcoin теперь создан с помощью приложения Green!

![GREEN 2FA MULTISIG](assets/fr/22.webp)

## Настройка 2FA

Нажмите на свою учетную запись.

![GREEN 2FA MULTISIG](assets/fr/23.webp)

Нажмите на зеленую кнопку "*Увеличить безопасность вашей учетной записи, добавив 2FA*".

![GREEN 2FA MULTISIG](assets/fr/24.webp)

После этого вы сможете выбрать метод аутентификации для доступа ко второму ключу вашей мультисигмы 2/2. В этом уроке мы будем использовать приложение для аутентификации. Если вы не знакомы с этим типом приложений, я рекомендую вам ознакомиться с нашим руководством по Authy:

https://planb.network/tutorials/others/general/authy-a76ab26b-71b0-473c-aa7c-c49153705eb7
Выберите "*Приложение для аутентификации*".

![GREEN 2FA MULTISIG](assets/fr/25.webp)

На зеленом экране появится QR-код и ключ восстановления. Этот ключ позволит вам восстановить доступ к 2FA в случае потери приложения Authy. Рекомендуется сделать надежную резервную копию этого ключа, хотя вы все равно сможете восстановить доступ к своим биткоинам после истечения срока блокировки, как объяснялось выше.

В приложении для аутентификации добавьте новый код, а затем отсканируйте QR-код, предоставленный Green.

![GREEN 2FA MULTISIG](assets/fr/26.webp)

*Очевидно, что вы никогда не должны делиться этим ключом и QR-кодом в Интернете, как это делаю я в данном руководстве. Этот образец кошелька будет использоваться только в Testnet и будет удален по окончании урока.*

Нажмите на кнопку "*Продолжить*".

![GREEN 2FA MULTISIG](assets/fr/27.webp)

Введите 6-значный динамический код, указанный в приложении для аутентификации.

![GREEN 2FA MULTISIG](assets/fr/28.webp)

двухфакторная аутентификация теперь включена.

![GREEN 2FA MULTISIG](assets/fr/29.webp)

В этом меню вы также можете установить продолжительность блокировки по времени. Этот отсчет начинается сразу после получения биткоинов, и по истечении срока блокировки ваши средства можно будет потратить только с помощью локального ключа, без необходимости использования 2FA. По умолчанию срок действия установлен на 12 месяцев, но для портфеля сбережений может иметь смысл выбрать 15 месяцев, чтобы минимизировать частоту обновления таймлока. И наоборот, для портфеля расходов может быть предпочтительнее 6-месячный таймлок, поскольку он будет часто обновляться при ежедневных операциях, а более короткий таймлок сократит время ожидания в случае проблем с 2FA. Вы сами определяете, какой срок блокировки вам больше подходит.

![GREEN 2FA MULTISIG](assets/fr/30.webp)

Теперь вы можете выйти из этого меню. Ваше портфолио multisig готово!

![GREEN 2FA MULTISIG](assets/fr/31.webp)

## Настройка портфеля на Blockstream Green

Если вы хотите персонализировать свое портфолио, нажмите на три маленькие точки в правом верхнем углу.

![GREEN 2FA MULTISIG](assets/fr/32.webp)

Опция "*Переименовать*" позволяет настроить название портфеля, что особенно удобно, если вы управляете несколькими портфелями в одном приложении.

![GREEN 2FA MULTISIG](assets/fr/33.webp)

Меню "*Unit*" позволяет изменить базовую единицу вашего кошелька. Например, вы можете выбрать отображение в сатоши, а не в биткоинах.

![GREEN 2FA MULTISIG](assets/fr/34.webp)

Меню "*Настройки*" предоставляет доступ к различным опциям вашего кошелька Bitcoin.

![GREEN 2FA MULTISIG](assets/fr/35.webp)

Здесь, например, вы найдете свой расширенный открытый ключ и его *дескриптор*, который пригодится, если вы планируете создать кошелек в режиме watch-only с этого кошелька.

![GREEN 2FA MULTISIG](assets/fr/36.webp)

Вы также можете изменить PIN-код своего кошелька и активировать биометрическое соединение.

![GREEN 2FA MULTISIG](assets/fr/37.webp)

## Использование Blockstream Green

Теперь, когда ваш кошелек Bitcoin настроен, вы готовы получить свои первые саты! Просто нажмите на кнопку "*Получить*".

![GREEN 2FA MULTISIG](assets/fr/38.webp)

Затем зеленый цвет отобразит первый пустой адрес приема в вашем кошельке. Вы можете либо отсканировать соответствующий QR-код, либо скопировать адрес напрямую, чтобы отправить биткоины. В адресах этого типа не указывается сумма, которую должен отправить плательщик. Однако вы можете сгенерировать адрес, запрашивающий определенную сумму, нажав на три маленькие точки в правом верхнем углу, затем на "*Запросить сумму*" и введя желаемую сумму.

![GREEN 2FA MULTISIG](assets/fr/39.webp)

Когда транзакция будет транслироваться в сети, она появится в вашем кошельке.

![GREEN 2FA MULTISIG](assets/fr/40.webp)

Подождите, пока вы не получите достаточно подтверждений, чтобы считать сделку окончательной.

![GREEN 2FA MULTISIG](assets/fr/41.webp)

Имея биткоины в кошельке, вы теперь можете также отправлять биткоины. Нажмите на кнопку "*Отправить*".

![GREEN 2FA MULTISIG](assets/fr/42.webp)

На следующей странице введите адрес получателя. Вы можете ввести его вручную или отсканировать QR-код.

![GREEN 2FA MULTISIG](assets/fr/43.webp)

Выберите сумму платежа.

![GREEN 2FA MULTISIG](assets/fr/44.webp)

В нижней части экрана вы можете выбрать размер комиссии для данной операции. У вас есть выбор: следовать рекомендациям приложения или установить свою комиссию. Чем выше комиссия по отношению к другим ожидающим транзакциям, тем быстрее будет обработана ваша транзакция. Информацию о рынке комиссий можно найти на сайте [Mempool.space](https://mempool.space/) в разделе "*Транзакционные сборы*".

![GREEN 2FA MULTISIG](assets/fr/45.webp)

Нажмите "*Следующее*", чтобы перейти к экрану сводки транзакций. Проверьте правильность адреса, суммы и расходов.

![GREEN 2FA MULTISIG](assets/fr/46.webp)

Если все прошло успешно, сдвиньте зеленую кнопку в нижней части экрана вправо, чтобы подписать и транслировать транзакцию в сети Bitcoin.

![GREEN 2FA MULTISIG](assets/fr/47.webp)

В этот момент вам нужно ввести код аутентификации, чтобы разблокировать второй мультисиг-ключ, принадлежащий Blockstream. Введите 6-значный код, отображаемый в приложении для аутентификации.

![GREEN 2FA MULTISIG](assets/fr/48.webp)

Теперь ваша транзакция появится на панели вашего кошелька Bitcoin и будет ожидать подтверждения.

![GREEN 2FA MULTISIG](assets/fr/49.webp)

Итак, теперь вы знаете, как легко настроить кошелек с мультисигмой 2/2, используя опцию 2FA от Blockstream Green!

Если вы нашли этот урок полезным, я буду благодарен, если вы оставите свой отзыв о нем ниже. Не стесняйтесь поделиться этой статьей в своих социальных сетях. Большое спасибо!

Я также рекомендую вам ознакомиться с другим исчерпывающим руководством по настройке мобильного приложения Blockstream Green для создания кошелька Liquid:

https://planb.network/tutorials/wallet/mobile/blockstream-green-liquid-b3e4fb82-902e-4782-ad2b-a61ab05a543a