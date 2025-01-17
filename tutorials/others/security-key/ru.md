---
name: YubiKey 2FA
description: Как использовать физический ключ безопасности?
---
![cover](assets/cover.webp)

В наше время двухфакторная аутентификация (2FA) стала необходимым условием для повышения безопасности онлайн-аккаунтов от несанкционированного доступа. С учетом роста кибератак, опираться только на пароль для защиты ваших аккаунтов иногда недостаточно.

2FA вводит дополнительный уровень безопасности, требуя второй формы аутентификации в дополнение к традиционному паролю. Эта верификация может принимать различные формы, такие как код, отправленный по SMS, динамический код, сгенерированный специализированным приложением, или использование физического ключа безопасности. Применение 2FA значительно снижает риски компрометации ваших аккаунтов, даже в случае утечки вашего пароля.

В другом уроке я объяснил, как настроить и использовать приложение 2FA TOTP:

https://planb.network/tutorials/others/general/authy-a76ab26b-71b0-473c-aa7c-c49153705eb7

Здесь мы рассмотрим, как использовать физический ключ безопасности в качестве второго фактора аутентификации для всех ваших аккаунтов.

## Что такое физический ключ безопасности?

Физический ключ безопасности — это устройство, используемое для повышения безопасности ваших онлайн-аккаунтов с помощью двухфакторной аутентификации (2FA). Эти устройства часто напоминают маленькие USB-ключи, которые необходимо вставить в порт компьютера для подтверждения, что это действительно законный пользователь пытается подключиться.
![SECURITY KEY 2FA](assets/notext/01.webp)
Когда вы входите в аккаунт, защищенный 2FA, и используете физический ключ безопасности, вам необходимо не только ввести ваш обычный пароль, но и вставить физический ключ безопасности в компьютер и нажать кнопку для подтверждения аутентификации. Таким образом, этот метод добавляет дополнительный уровень безопасности, потому что даже если кто-то узнает ваш пароль, он не сможет получить доступ к вашему аккаунту без физического владения ключом.

Физический ключ безопасности особенно эффективен, потому что он сочетает в себе два разных типа факторов аутентификации: доказательство знания (пароль) и доказательство владения (физический ключ).

Однако у этого метода 2FA также есть недостатки. Во-первых, вам всегда нужно иметь при себе ключ безопасности, если вы хотите получить доступ к своим аккаунтам. Возможно, вам придется добавить его к своему связке ключей. Во-вторых, в отличие от других методов 2FA, использование физического ключа безопасности влечет за собой начальные затраты, поскольку вам нужно приобрести это маленькое устройство. Цена ключей безопасности обычно варьируется от €30 до €100 в зависимости от выбранных функций.

## Какой физический ключ безопасности выбрать?

При выборе ключа безопасности необходимо учитывать несколько критериев.
Прежде всего, вам нужно проверить поддерживаемые устройством протоколы. Как минимум, я советую выбирать ключ, поддерживающий OTP, FIDO2 и U2F. Эти детали обычно выделяют производители в описаниях продуктов. Чтобы проверить совместимость каждого ключа, вы также можете посетить [dongleauth.com](https://www.dongleauth.com/dongles/).
Также убедитесь, что ключ совместим с вашей операционной системой, хотя известные бренды, такие как Yubikey, обычно поддерживают все широко используемые системы.

Вы также должны выбрать ключ в зависимости от типа портов, доступных на вашем компьютере или смартфоне. Например, если ваш компьютер имеет только порты USB-C, выберите ключ с разъемом USB-C. Некоторые ключи также предлагают варианты подключения через Bluetooth или NFC.
![SECURITY KEY 2FA](assets/notext/02.webp)
Вы также можете сравнивать устройства на основе их дополнительных функций, таких как водонепроницаемость и устойчивость к пыли, а также форма и размер ключа.
Относительно брендов ключей безопасности, Yubico является наиболее известным с его устройствами [YubiKey](https://www.yubico.com/), которые я лично использую и рекомендую. Google также предлагает устройство [Titan Security Key](https://store.google.com/fr/product/titan_security_key). Что касается альтернатив на основе открытого исходного кода, [SoloKeys](https://solokeys.com/) (не OTP) и [NitroKey](https://www.nitrokey.com/products/nitrokeys) представляют интерес, но у меня никогда не было возможности их протестировать.
## Как использовать физический ключ безопасности?

После получения вашего ключа безопасности никаких специальных настроек не требуется. Ключ обычно готов к использованию сразу после получения. Вы можете немедленно использовать его для защиты ваших онлайн-аккаунтов, поддерживающих этот тип аутентификации. Например, я покажу вам, как защитить мой аккаунт Proton mail с помощью этого физического ключа безопасности.
![SECURITY KEY 2FA](assets/notext/03.webp)
Вы найдете опцию активации 2FA в настройках вашего аккаунта, часто в разделе "*Пароль*" или "*Безопасность*". Нажмите на флажок или кнопку, которая позволяет активировать 2FA с физическим ключом.
![SECURITY KEY 2FA](assets/notext/04.webp)
Подключите ваш ключ к компьютеру.
![SECURITY KEY 2FA](assets/notext/05.webp)
Нажмите кнопку на вашем ключе безопасности для подтверждения.
![SECURITY KEY 2FA](assets/notext/06.webp)
Введите имя, чтобы помнить, какой ключ вы использовали.
![SECURITY KEY 2FA](assets/notext/07.webp)
И вот, ваш ключ безопасности успешно добавлен для аутентификации 2FA вашего аккаунта.
![SECURITY KEY 2FA](assets/notext/08.webp)
В моем примере, если я попытаюсь снова подключиться к моему аккаунту Proton mail, мне сначала будет предложено ввести мой пароль вместе с именем пользователя. Это первый фактор аутентификации.
![SECURITY KEY 2FA](assets/notext/09.webp)
Затем мне будет предложено подключить мой ключ безопасности для второго фактора аутентификации.
![SECURITY KEY 2FA](assets/notext/10.webp)
Далее, мне нужно нажать кнопку на физическом ключе для подтверждения аутентификации, и я снова подключен к моему аккаунту Proton mail.
![SECURITY KEY 2FA](assets/notext/11.webp)
Повторите эту операцию для всех онлайн-аккаунтов, которые вы хотите защитить таким образом, особенно для критически важных аккаунтов, таких как ваши электронные почты, менеджеры паролей, облачные и онлайн-сервисы хранения данных или финансовые аккаунты.