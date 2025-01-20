---
term: OP_TUCK (0X7D)

---
Копирует элемент в верхней части стека и вставляет его между вторым и третьим элементами стека. Например, если стек имеет вид:

```text
A
B
C
D
```

`OP_TUCK` продублирует верхний элемент `A` и поместит его в третью позицию. В результате будет получен стек:

```text
A
B
A
C
D
```