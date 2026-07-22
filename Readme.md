# Módulo 1 – Introdução ao Dart
- História do Dart
- Como o Dart funciona
- Compilação JIT x AOT
- Instalação
- Estrutura de um programa

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
Quando chega o momento de publicar o aplicativo:<br>
''' Dart
dart code
      ↓
Compilação
      ↓
Código Nativo Android/iOS
'''<br>
Nesse modo, o aplicativo fica muito mais rápido.

## Comparação
| Desenvolvimento   | Produção           |
| ----------------- | ------------------ |
| JIT               | AOT                |
| Hot Reload        | Máxima performance |
| Compilação rápida | Código otimizado   |