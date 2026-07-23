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

## Operadores Relacionais e Lógicos

### Operadores relacionais
Os operadores relacionais comparam valores e retornam um resultado booleano (true ou false).

**Analogia**

Imagine que um porteiro está controlando a entrada de um evento.

Ele recebe algumas perguntas:

- A pessoa é maior de 18 anos?
- Possui ingresso?
- Está na lista de convidados?

Cada resposta só pode ser:

- Sim (true)
- Não (false)

### Operadores Relacionais
| Operador | Significado    |
| -------- | -------------- |
| `==`     | Igual a        |
| `!=`     | Diferente de   |
| `>`      | Maior que      |
| `<`      | Menor que      |
| `>=`     | Maior ou igual |
| `<=`     | Menor ou igual |

**Igual `=`**
``` dart
void main() {
  int idade = 18;

  print(idade == 18);
}
```

**Diferente (`!=`)**
``` dart
print(10 != 5);
```

**Maior que (`>`)**
``` dart
print(20 > 10);
```

**Menor que (`<`)**
``` dart
print(5 < 8);
```