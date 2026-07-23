# Módulo 2 – Operadores em Dart

## Operadores Aritméticos
Os operadores aritméticos em Dart executam cálculos matemáticos básicos e avançados, incluindo adição (+), subtração (-), multiplicação (*) e divisão (/).

``` dart
| Operador | Significado      |
| -------- | ---------------- |
| `+`      | Soma             |
| `-`      | Subtração        |
| `*`      | Multiplicação    |
| `/`      | Divisão          |
| `%`      | Resto da divisão |
| `~/`     | Divisão inteira  |
```
### Divisão Inteira (~/)
Esse operador existe em poucas linguagens e é bastante usado no Dart. Ele descarta a parte decimal.
``` dart
print(10 ~/ 3);
```
Resultado
``` dart
3
```

### Módulo (%)
Esse operador retorna o resto da divisão.

**Para que serve %?**

Um dos usos mais comuns é descobrir se um número é par ou ímpar.
``` dart
if (numero % 2 == 0) {
  print("Par");
}
```

## Boas Práticas
Evite escrever expressões muito complexas em uma única linha.

Em vez de:
``` dart
resultado = a + b * c - d / e + f * g;
```

Quebre em etapas:
``` dart
var multiplicacao = b * c;
var divisao = d / e;
var resultado = a + multiplicacao - divisao + (f * g);
```
O código fica mais legível e mais fácil de manter.