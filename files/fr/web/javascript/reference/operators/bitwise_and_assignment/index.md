---
title: Affectation après ET binaire (&=)
slug: Web/JavaScript/Reference/Operators/Bitwise_AND_assignment
---

{{jsSidebar("Operators")}}

L'opérateur d'affectation après ET binaire (`&=`) utilise la représentation binaire des deux opérandes, applique un ET logique entre chaque puis affecte le résultat de l'opération à la variable représentée par l'opérande gauche.

{{InteractiveExample("JavaScript Demo: Expressions - Bitwise AND assignment")}}

```js interactive-example
let a = 5; // 00000000000000000000000000000101
a &= 3; // 00000000000000000000000000000011

console.log(a); // 00000000000000000000000000000001
// Expected output: 1
```

## Syntaxe

```js
Opérateur: x &= y;
Signification: x = x & y;
```

## Exemples

### Utiliser l'affectation après ET binaire

```js
let a = 5;
// 5:     00000000000000000000000000000101
// 2:     00000000000000000000000000000010
a &= 2; // 0
```

## Spécifications

{{Specifications}}

## Compatibilité des navigateurs

{{Compat}}

## Voir aussi

- [Les opérateurs d'affectation dans le guide JavaScript](/fr/docs/Web/JavaScript/Guide/Expressions_and_operators#assignment)
- [L'opérateur ET binaire](/fr/docs/Web/JavaScript/Reference/Operators/Bitwise_AND)
