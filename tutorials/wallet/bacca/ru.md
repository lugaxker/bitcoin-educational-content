---
name: Bacca
description: Настройка бухгалтерской книги без программы Ledger Live
---
![cover](assets/cover.webp)

Если вы используете Ledger, то наверняка сталкивались с тем, что для проверки подлинности устройства и установки на него приложения Bitcoin необходимо использовать программу Ledger Live, по крайней мере, для первоначальной настройки. Однако после такой настройки многие биткоинщики предпочитают использовать специализированное программное обеспечение для управления биткоин-кошельками, например Sparrow или Liana, а не Ledger Live. Хотя компания Ledger производит отличные аппаратные кошельки, которые быстро включают в себя новейшие функции Биткойна, их программное обеспечение не всегда адаптировано к специфическим потребностям биткойнеров. Действительно, Ledger Live включает в себя множество функций, предназначенных для альткоинов, в то время как возможности управления биткоин-кошельком ограничены. Но проблема Sparrow и Liana (на данный момент) в том, что они не позволяют установить приложение Bitcoin на Ledger.

Чтобы обойти необходимость использования Ledger Live при первоначальной настройке вашего Ledger, вы можете воспользоваться инструментом Bacca (или "Установщик Ledger"). Это программное обеспечение позволяет устанавливать и обновлять приложение Bitcoin, проверять подлинность вашего Ledger и даже впоследствии обновлять прошивку устройства. Bacca была создана Антуаном Пуансо (Darosior), разработчиком Bitcoin Core в Chaincode Labs, соучредителем [компаний Revault и Liana] (https://wizardsardine.com/) и Pythcoiner.

В этом руководстве я покажу вам, как использовать этот инструмент, чтобы вы могли навсегда обойтись без программы Ledger Live и по-прежнему пользоваться устройствами Ledger. Он работает на всех устройствах: Nano S Classic, Nano S Plus, Nano X, Flex и Stax.

---
*Обратите внимание, что этот инструмент довольно новый, и его разработчики указывают, что он все еще находится **на стадии тестирования**. Они рекомендуют использовать его только в тестовых целях, а не в качестве устройства, предназначенного для размещения реального кошелька Bitcoin, хотя это вполне возможно. В связи с этим я рекомендую вам следовать рекомендациям разработчиков этого инструмента, которые указаны [в README их репозитория на GitHub](https://github.com/darosior/ledger_installer).*

---
## Пререквизиты

На компьютере вам понадобятся два инструмента для работы с Bacca:


- Git ;
- Ржавчина.

Если вы уже установили их, этот шаг можно пропустить.

**Linux:**

В дистрибутиве Linux Git обычно предустановлен. Чтобы проверить, установлен ли Git в вашей системе, вы можете ввести в терминале следующую команду :

```bash
git --version
```

Если в вашей системе не установлен Git, вот команда для его установки на Debian:

```bash
sudo apt install git
```

Наконец, чтобы установить среду разработки Rust, выполните команду :

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

**Windows:**

Чтобы установить Git, перейдите на [официальный сайт проекта](https://git-scm.com/). Загрузите программу и следуйте инструкциям по установке.

![BACCA](assets/fr/01.webp)

Выполните те же действия, что и при установке Rust с [официального сайта](https://www.rust-lang.org/tools/install).

![BACCA](assets/fr/02.webp)

**MacOS:**

Если Git еще не установлен в вашей системе, откройте терминал и выполните следующую команду для его установки:

```bash
git --version
```

Если Git не установлен в вашей системе, откроется окно с предложением установить Xcode, в который входит Git. Просто следуйте инструкциям на экране, чтобы продолжить установку.

Чтобы установить Rust, выполните следующую команду:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

## Установка Bacca

Откройте терминал и перейдите в папку, в которой вы хотите сохранить программу, а затем выполните следующую команду:

```bash
git clone https://github.com/darosior/ledger_installer.git
```

Перейдите в каталог программного обеспечения:

```bash
cd ledger_installer
```

Затем используйте Cargo для компиляции проекта и запуска графического интерфейса Bacca:

```bash
cargo run -p ledger_manager_gui
```

Теперь у вас есть доступ к интерфейсу программы.

![BACCA](assets/fr/03.webp)

## Настройка бухгалтерской книги

Прежде чем начать, если ваш Ledger новый, убедитесь, что вы настроили PIN-код и сохранили фразу восстановления. Для этих начальных шагов вам не нужна программа Ledger Live. Просто подключите Ledger к питанию через USB-кабель. Если вы не знаете, как выполнить эти два шага, обратитесь к началу руководства по конкретной модели:

https://planb.network/tutorials/wallet/hardware/ledger-c6fc7d82-91e7-4c74-bad7-cbff7fea7a88
https://planb.network/fr/tutorials/wallet/hardware/ledger-nano-s-plus-75043cb3-2e8e-43e8-862d-ca243b8215a4
https://planb.network/fr/tutorials/wallet/hardware/ledger-flex-3728773e-74d4-4177-b39f-bd923700c76a
## Использование Бакки

Подключите Ledger к компьютеру и разблокируйте его с помощью установленного PIN-кода. Bacca автоматически обнаружит ваш Ledger.

![BACCA](assets/fr/04.webp)

Чтобы подтвердить подлинность вашего устройства Ledger, нажмите на кнопку "*Проверка*". Чтобы продолжить, необходимо авторизовать соединение на устройстве Ledger.

![BACCA](assets/fr/05.webp)

После этого Bacca сообщит вам, является ли ваш Ledger подлинным. Если нет, это свидетельствует либо о том, что устройство было взломано, либо о том, что это подделка. В этом случае немедленно прекратите его использование.

![BACCA](assets/fr/06.webp)

В меню "*Приложения*" вы можете просмотреть список приложений, уже установленных на вашем Ledger.

![BACCA](assets/fr/07.webp)

Чтобы установить приложение Bitcoin, нажмите на "*Install*", затем авторизуйте установку на вашем Ledger.

![BACCA](assets/fr/08.webp)

Приложение хорошо устанавливается.

![BACCA](assets/fr/09.webp)

Если у вас установлена не самая последняя версия приложения Bitcoin, Bacca отобразит кнопку "*Обновить*" вместо индикации "*Самая последняя*". Просто нажмите на эту кнопку, чтобы обновить приложение.

![BACCA](assets/fr/10.webp)

Теперь, когда ваш Ledger правильно настроен с последней версией приложения Bitcoin, вы готовы импортировать и использовать свой кошелек в таких программах управления, как Sparrow или Liana, без необходимости проходить через Ledger Live!

Если вы нашли этот урок полезным, я буду благодарен, если вы оставите свой отзыв о нем ниже. Не стесняйтесь поделиться этой статьей в своих социальных сетях. Большое спасибо!

Я также рекомендую вам взглянуть на этот учебник по GnuPG, в котором рассказывается о том, как проверить целостность и подлинность программного обеспечения перед его установкой. Это очень важная практика, особенно при установке программ для управления портфелем, таких как Liana или Sparrow:

https://planb.network/tutorials/others/general/integrity-authenticity-21d0420a-be02-4663-94a3-8d487f23becc