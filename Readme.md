# Módulo 1 – Introdução ao Dart

## Conteúdo
- O que é Dart
- Estrutura de um programa
- Variáveis
- Tipos de dados
- var
- dynamic
- final
- const

## Objetivos
- Criar programas simples em Dart.
- Declarar variáveis.
- Escolher corretamente entre var, final e const.
- Entender a inferência de tipos.

## O que é o Dart?

O Dart é uma linguagem de programação criada pelo Google em 2011.

Ela foi projetada para ser:

Simples de aprender
Muito rápida
Orientada a Objetos
Fortemente tipada
Excelente para desenvolvimento de interfaces gráficas (UI)

Hoje, o principal uso do Dart é o desenvolvimento de aplicações com Flutter, mas também pode ser utilizado para criar aplicações web, desktop, servidores e ferramentas de linha de comando.

## Como o Dart funciona?
Ele possui dois modos principais de compilação.

### JIT (Just-In-Time)
Durante o desenvolvimento, o Dart compila o código "na hora".
Isso permite o famoso Hot Reload.
Você altera o código...
↓
O aplicativo atualiza quase instantaneamente.
Sem recompilar todo o projeto.

### AOT (Ahead-Of-Time)
Quando chega o momento de publicar o aplicativo:

```
dart code
      ↓
Compilação
      ↓
Código Nativo Android/iOS
```

Nesse modo, o aplicativo fica muito mais rápido.

## Comparação
| Desenvolvimento   | Produção           |
| ----------------- | ------------------ |
| JIT               | AOT                |
| Hot Reload        | Máxima performance |
| Compilação rápida | Código otimizado   |

# Declaração de Váriaveis em Dart

## Inferência ou Dedução de Tipos
O Dart consegue descobrir automaticamente o tipo de váriavel utilizando a inferência ou dedução de tipos, utiliza a declaração **var**.

Ao invés de escrever:
``` dart
String nome = "Bruno";
```
Você pode escrever:
``` dart
var nome = "Bruno";
```

O compilador irá entender que a váriavel é uma string.

A mesma coisa acontece com os outros tipos de váriaveis, int, boolean, double.

**Devo sempre usar o *var*?**

Não! Você deve utilizar quando o tipo é óbvio, ex:

``` dart
var nome = "João";
```

Outro exemplo:
``` dart
var idade = 28;
```

## Tipo Dynamic
No Dart, a declaração do tipo **dynamic** serve para indicar que uma variável pode armazenar qualquer tipo de dado e que o seu valor pode mudar para outro tipo diferente durante a execução do programa. Para usá-la, basta escrever a palavra-chave dynamic antes do nome da variável:

``` dart
dynamic valor = "João";
```
A mesma váriavel agora pode ter valores de outros tipos:
``` dart
valor = 25
```

**Isso é bom? Não é?**

Na maioria das vezes não! Exemplo:
``` dart
dynamic nome = "Bruno";
print(nome.toUpperCase());

nome = 20;
print(nome.toUpperCase());
```

Na segunda chamada ocorrerá um erro em tempo de execução, pois um int não possui o método toUpperCase().

**E por que usar *dynamic* então?**

Há situações em que ele é útil, por exemplo:

- Ler dados de uma API.
- Trabalhar com JSON antes da conversão para objetos.
- Interagir com bibliotecas onde o tipo não é conhecido.

Mesmo assim, tenha consciência e use com moderação.

## Variáveis Imutaveis em Dart
### final

Uma variável declarada com **final** pode receber um valor apenas uma única vez. Após a inicialização, qualquer tentativa de atribuir um novo valor resulta em erro de compilação.
``` dart
final nome = "Bruno";
nome = "Carlos";
```

**Quando usar?** Sempre que um valor será definido apenas uma vez durante a execução.

### const
Em Dart, a palavra-chave const define uma constante em tempo de compilação, o que significa que o seu valor precisa ser totalmente conhecido antes de o programa rodar. Ela se diferencia de final (que aceita valores definidos em tempo de execução) e de var (que permite mudanças).
``` dart
const pi = 3.14 
```