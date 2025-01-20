---
term: ВОЛОКНО

---
Аббревиатура от "*Fast Internet Bitcoin Relay Engine*". Это протокол, разработанный Мэттом Коралло в 2016 году для ускорения распространения блоков Биткойна по всему миру. Его целью было сокращение задержек при распространении как можно ближе к физическим пределам. FIBRE был призван обеспечить более справедливое распределение возможностей для майнинга, чтобы доля блоков, добытых участником, точно отражала его вклад в вычислительную мощность, независимо от его положения в сети.

Действительно, задержка при передаче блоков может благоприятствовать крупным, хорошо связанным группам майнеров, часто расположенным близко друг к другу, в ущерб более мелким. Со временем это явление может привести к усилению централизации майнинга и снижению общей безопасности системы. Для решения этой проблемы в FIBRE были введены коды коррекции ошибок и передача дополнительных данных для компенсации потерь пакетов, а также использование компактных блоков, подобных тем, что описаны в BIP152, и все это работало через UDP, чтобы обойти некоторые ограничения TCP. Тем не менее, от FIBRE отказались в 2020 году, в основном из-за ее зависимости от одного сопровождающего и того факта, что принятие BIP152 сделало такую систему менее необходимой.