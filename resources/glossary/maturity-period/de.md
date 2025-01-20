---
term: FÄLLIGKEIT

---
Die notwendige Verzögerung, bevor eine Blockbelohnung vom Miner, der sie erhalten hat, ausgegeben werden kann. Dieser Zeitraum ist auf 100 Blöcke nach dem geminten Block festgelegt, was 101 Bestätigungen für die Coinbase-Transaktion entspricht. Während dieser Zeit können die neu geschaffenen Bitcoins in der Blockbelohnung nicht ausgegeben werden. Der Zweck dieser Regel besteht darin, Komplikationen im Zusammenhang mit der Verwendung von Bitcoins aus einer Kette zu vermeiden, die später veraltet sein könnte. Es kommt nämlich vor, dass gültige Blöcke irgendwann ungültig werden, wenn ein anderer Block in gleicher Höhe in eine Kette aufgenommen wird, an der mehr Arbeit geleistet wurde. Dieses Phänomen, das als Reorganisation bekannt ist, führt zur Schaffung eines "verwaisten Blocks" oder "veralteten Blocks", wodurch dem Schürfer die Bitcoins entzogen werden, die in der Coinbase des verlassenen Blocks enthalten sind. Wären die neu geschaffenen Bitcoins sofort ausgabefähig, könnte jede Transaktion mit ihnen rückwirkend annulliert werden, was zu Verlusten für die Inhaber dieser Bitcoins führt. Ein solches Szenario könnte zu einer Kaskade von Annullierungen ansonsten gültiger Transaktionen führen und damit alle an dieser Transaktionskette beteiligten Nutzer in Mitleidenschaft ziehen. Die Laufzeit ist daher ein Präventivmechanismus gegen dieses Risiko. Durch eine Verzögerung von 100 Blöcken, bevor die neu ausgegebenen Bitcoins verwendet werden können, wird verhindert, dass Münzen aus Blöcken, die schließlich für ungültig erklärt werden, im Umlauf sind und andere Transaktionen beeinträchtigen. Die Wahrscheinlichkeit einer Umstrukturierung über 101 Blöcke hinweg ist so gering, dass sie als vernachlässigbar angesehen wird.