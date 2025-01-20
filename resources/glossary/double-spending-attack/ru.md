---
term: ДВОЙНЫЕ РАСХОДЫ (АТАКА)

---
Атака, при которой злоумышленник пытается использовать один и тот же UTXO (*Unspent Transaction Output*) более одного раза, чтобы обогатиться за счет сторон, участвующих в транзакциях. В принципе, как только транзакция подтверждается в блоке и добавляется в блокчейн, использование этих биткоинов навсегда записывается, предотвращая любые дальнейшие траты тех же самых биткоинов. Предотвращение двойных трат - это даже основная польза блокчейна.

В контексте атаки "двойной траты" злоумышленник сначала совершает законную транзакцию с продавцом, а затем создает вторую конкурирующую транзакцию, расходуя те же монеты, либо отправляя их обратно себе, чтобы вернуть сумму, либо используя их для покупки другого товара или услуги у другого продавца.

Существует два основных сценария, по которым может быть осуществлена эта атака. Первый, самый простой для злоумышленника, предполагает проведение мошеннической транзакции до того, как законная транзакция будет включена в блок. Чтобы гарантировать, что мошенническая транзакция будет подтверждена первой, злоумышленник привязывает к ней значительно более высокую комиссию за транзакцию, чем к законной. Это своего рода мошеннический RBF. Такой сценарий возможен только в том случае, если продавец соглашается завершить продажу в "нулевом режиме", то есть без каких-либо подтверждений платежной операции. Именно поэтому настоятельно рекомендуется дождаться нескольких подтверждений, прежде чем считать транзакцию неизменяемой. Второй сценарий, гораздо более сложный, - это атака на 51 %. Если злоумышленник контролирует значительную часть вычислительных мощностей сети, он может создать конкурирующую цепочку, содержащую законную транзакцию, но включающую его мошенническую транзакцию. Когда торговец примет сделку, а злоумышленнику удастся создать более длинную цепочку (с большим количеством накопленной работы), чем законная, он может транслировать свою мошенническую цепочку, которая будет признана узлами сети как действительная.