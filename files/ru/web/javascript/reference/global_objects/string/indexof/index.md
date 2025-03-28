---
title: String.prototype.indexOf()
slug: Web/JavaScript/Reference/Global_Objects/String/indexOf
---

{{JSRef}}

## Сводка

Метод **`indexOf()`** возвращает индекс первого вхождения указанного значения в строковый объект {{jsxref("Global_Objects/String", "String")}}, на котором он был вызван, начиная с индекса `fromIndex`. Возвращает -1, если значение не найдено.

{{InteractiveExample("JavaScript Demo: String.indexOf()", "taller")}}

```js interactive-example
const paragraph = "I think Ruth's dog is cuter than your dog!";

const searchTerm = "dog";
const indexOfFirst = paragraph.indexOf(searchTerm);

console.log(`The index of the first "${searchTerm}" is ${indexOfFirst}`);
// Expected output: "The index of the first "dog" is 15"

console.log(
  `The index of the second "${searchTerm}" is ${paragraph.indexOf(
    searchTerm,
    indexOfFirst + 1,
  )}`,
);
// Expected output: "The index of the second "dog" is 38"
```

## Синтаксис

```js-nolint
indexOf(searchString)
indexOf(searchString, position)
```

### Параметры

- `searchValue`
  - : Строка, представляющая искомое значение.
- `fromIndex`
  - : Необязательный параметр. Местоположение внутри строки, откуда начинать поиск. Может быть любым целым числом. Значение по умолчанию установлено в 0. Если `fromIndex < 0`, поиск ведётся по всей строке (так же, как если бы был передан 0). Если `fromIndex >= str.length`, метод вернёт -1, но только в том случае, если `searchValue` не равен пустой строке, в этом случае он вернёт `str.length`.

## Описание

Символы в строке идут слева направо. Индекс первого символа равен 0, а последнего символа в строке `stringName` равен `stringName.length - 1`.

```js
"Синий кит".indexOf("Синий"); // вернёт  0
"Синий кит".indexOf("Голубой"); // вернёт -1
"Синий кит".indexOf("кит", 0); // вернёт  6
"Синий кит".indexOf("кит", 5); // вернёт  6
"Синий кит".indexOf("", 8); // вернёт  8
"Синий кит".indexOf("", 9); // вернёт 9
"Синий кит".indexOf("", 10); // вернёт 9
```

### Регистрозависимость

Метод `indexOf()` является регистрозависимым. Например, следующее выражение вернёт -1:

```js
"Синий кит".indexOf("синий"); // вернёт -1
```

### Проверка на вхождение

Обратите внимание, что значение 0 не вычисляется в `true`, а значение -1 не вычисляется в `false`. Поэтому, для проверки того, что конкретная строка содержится в другой строке, правильно делать так:

```js
"Синий кит".indexOf("Синий") !== -1; // true
"Синий кит".indexOf("Голубой") !== -1; // false
```

## Примеры

### Пример: использование методов `indexOf()` и `lastIndexOf()`

В следующем примере используются методы `indexOf()` и {{jsxref("String.prototype.lastIndexOf()", "lastIndexOf()")}} для нахождения значений в строке `"Дивный новый мир"`.

```js
var anyString = "Дивный новый мир";

console.log(
  "Индекс первого вхождения «й» с начала строки равен " +
    anyString.indexOf("й"),
);
// Отобразит 5
console.log(
  "Индекс первого вхождения «й» с конца строки равен " +
    anyString.lastIndexOf("й"),
);
// Отобразит 11

console.log(
  "Индекс вхождения «новый» с начала строки равен " +
    anyString.indexOf("новый"),
);
// Отобразит 7
console.log(
  "Индекс вхождения «новый» с конца строки равен " +
    anyString.lastIndexOf("новый"),
);
// Отобразит 7
```

### Пример: метод `indexOf()` и регистрозависимость

В следующем примере определяются две строковых переменных. Переменные содержат одинаковые строки, за исключение того, что слова во второй строке начинаются с заглавных букв. Первый вызов метода {{domxref("console.log()")}} отобразит 18. Но поскольку метод `indexOf()` является регистрозависимым, строка `"чеддер"` в переменной `myCapString` не будет найдена, так что второй вызов метода `console.log()` отобразит -1.

```js
var myString = "бри, пеппер джек, чеддер";
var myCapString = "Бри, Пеппер Джек, Чеддер";

console.log(
  'Вызов myString.indexOf("чеддер") вернул ' + myString.indexOf("чеддер"),
);
// Отобразит 18
console.log(
  'Вызов myCapString.indexOf("чеддер") вернул ' + myCapString.indexOf("чеддер"),
);
// Отобразит -1
```

### Пример: использование метода `indexOf()` для подсчёта вхождений буквы в строку

Следующий пример устанавливает значение переменной `count` в количество вхождений буквы `в` в строку `str`:

```js
var str = "Быть или не быть, вот в чём вопрос.";
var count = 0;
var pos = str.indexOf("в");

while (pos !== -1) {
  count++;
  pos = str.indexOf("в", pos + 1);
}

console.log(count); // отобразит 3
```

## Спецификации

{{Specifications}}

## Совместимость с браузерами

{{Compat}}

## Смотрите также

- {{jsxref("String.prototype.charAt()")}}
- {{jsxref("String.prototype.lastIndexOf()")}}
- {{jsxref("String.prototype.split()")}}
- {{jsxref("Array.prototype.indexOf()")}}
