---
term: BIP

---
Аббревиатура от "Bitcoin Improvement Proposal" Bitcoin Improvement Proposal (BIP) - это формальный процесс для предложения и документирования улучшений и изменений в протоколе Bitcoin и его стандартах. Поскольку в Биткойне нет центрального органа, принимающего решения об обновлениях, BIP позволяют сообществу предлагать, обсуждать и внедрять улучшения структурированным и прозрачным образом. В каждом BIP подробно описываются цели предлагаемого улучшения, обоснования, потенциальное влияние на совместимость, а также преимущества и недостатки. BIP могут быть написаны любым членом сообщества, но должны быть одобрены другими разработчиками и редакторами, которые поддерживают базу данных Bitcoin Core на GitHub: Брайан Бишоп, Джон Атак, Люк Дашжр, Марк Эрхардт (Мерч), Олаолува Осунтокун и Рубен Сомсен. Однако важно понимать, что роль этих людей в редактировании BIPs не означает, что они контролируют Bitcoin. Если кто-то предложит улучшение, которое не будет принято в рамках формального процесса BIP, он все равно сможет представить его непосредственно сообществу Биткойна или даже создать форк, включающий его модификацию. Преимущество процесса BIP заключается в его формальности и централизации, которые способствуют обсуждению, чтобы избежать разногласий между пользователями Биткойна, стремящимися внедрять обновления на основе консенсуса. В конечном итоге именно принцип экономического большинства определяет динамику власти внутри протокола.

BIP делятся на три основные категории:


- Стандартные BIP*: Относятся к модификациям, которые непосредственно влияют на реализацию Биткойна, например, к правилам проверки транзакций и блоков;
- Информационные BIP*: Предоставляют информацию или рекомендации, не предлагая прямых изменений в протоколе;
- Процессы BIPs*: Опишите изменения в процедурах, связанных с биткойном, например, в процессах управления.

Стандартные и информационные BIP также классифицируются по "Layer":


- Уровень консенсуса*: BIP на этом уровне касаются правил консенсуса Биткойна, например, модификации блока или правил проверки транзакций. Эти предложения могут быть как мягкими форками (модификации, совместимые с обратным ходом событий), так и жесткими форками (модификации, не совместимые с обратным ходом событий). Например, BIP для SegWit и Taproot относятся к этой категории;
- Службы пиров*: Этот уровень связан с работой сети узлов Биткойна, то есть с тем, как узлы находят и общаются друг с другом в Интернете.
- API/RPC*: BIPs этого уровня относятся к интерфейсам прикладного программирования (API) и удаленным вызовам процедур (RPC), которые позволяют программному обеспечению Биткойна взаимодействовать с узлами;
- Уровень приложений*: Этот уровень относится к приложениям, созданным на основе Биткойна. BIP в этой категории обычно касаются модификаций на уровне стандартов кошельков Bitcoin.

Процесс подачи BIP начинается с разработки концепции и обсуждения идеи в списке рассылки *Bitcoin-dev*. Если идея перспективна, автор составляет проект BIP в соответствии с определенным форматом и отправляет его через Pull Request в репозиторий Core на GitHub. Редакторы рассматривают это предложение, чтобы убедиться, что оно соответствует всем критериям. BIP должен быть технически осуществимым, полезным для протокола, соответствовать требуемому формату и философии Биткойна. Если BIP соответствует этим условиям, он официально включается в репозиторий BIP на GitHub. Затем ему присваивается номер. Этот номер обычно определяется редактором, чаще всего Люком Дэшджром, и присваивается логически: BIP, посвященные схожим темам, часто получают последовательные номера.

В течение своего жизненного цикла BIP проходят через различные статусы. Текущий статус указывается в заголовке каждого BIP:


- Проект: Предложение все еще находится на стадии разработки и обсуждения;
- Предлагается: BIP считается завершенным и готов к рассмотрению сообществом;
- Отложено: BIP откладывается на потом чемпионом или редактором;
- Отклонено: BIP классифицируется как отклоненный, если он не проявлял никакой активности в течение 3 лет. Его автор может решить возобновить его позже, что позволит ему вернуться в статус проекта;
- Отозвано: BIP был отозван его автором;
- Финал: BIP принят и широко внедрен в Биткойн;
- Активный: Этот статус присваивается только для процессуальных BIP, когда достигается определенный консенсус;
- Заменено / Устарело: BIP больше не применяется или был заменен более новым предложением, которое делает его ненужным.

![](../../dictionnaire/assets/25.webp)

> ► *BIP - это аббревиатура от "Bitcoin Improvement Proposal". На французский язык его можно перевести как "Предложение по улучшению Биткойна". Однако в большинстве французских текстов аббревиатура "BIP" используется как существительное общего рода, иногда женского, иногда мужского*