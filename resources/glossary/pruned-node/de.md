---
term: PRUNED NODE

---
Ein Pruned Node, auf Englisch "Pruned Node", ist ein vollständiger Knoten, der eine Bereinigung der Blockchain vornimmt. Dabei werden nach und nach die ältesten Blöcke entfernt, nachdem sie ordnungsgemäß verifiziert wurden, um nur die jüngsten Blöcke zu behalten. Die Aufbewahrungsgrenze wird in der Datei "bitcoin.conf" über den Parameter "prune=n" angegeben, wobei "n" die maximale Größe der Blöcke in Megabyte (MB) ist. Wenn nach diesem Parameter "0" angegeben wird, wird das Pruning deaktiviert und der Knoten behält die gesamte Blockchain bei.

Abgeschnittene Knoten werden manchmal als andere Arten von Knoten als vollständige Knoten betrachtet. Die Verwendung eines Pruned Nodes kann besonders für Nutzer interessant sein, die mit Einschränkungen bei der Speicherkapazität konfrontiert sind. Derzeit muss ein Full Node fast 600 GB nur für die Speicherung der Blockchain haben. Ein Pruned Node kann den benötigten Speicherplatz auf bis zu 550 MB begrenzen. Obwohl er weniger Speicherplatz verbraucht, bietet ein Pruned Node ein ähnliches Maß an Verifizierung und Validierung wie ein Full Node. Pruned Nodes bieten ihren Nutzern daher mehr Vertrauen im Vergleich zu Light Nodes (SPV).