---
title: Int32Array() constructor
slug: Web/JavaScript/Reference/Global_Objects/Int32Array/Int32Array
---

{{JSRef}}

**`Int32Array`** 형식화 배열(TypedArray) 생성자는 플랫폼의 바이트 순서를 따르는 2의 보수 32비트의 부호있는 정수
배열을 생성합니다. 바이트 순서를 제어해야 하는 경우 대신 {{jsxref("DataView")}}를 사용합니다. 배열의 내용은 0으로
초기화됩니다. 배열이 생성되면 객체의 메서드를 사용하거나 표준 배열 인덱스 구문(즉, 대괄호 표기법 사용)을 사용하여 배열의 요소를
참조할 수있습니다.

## 구문

```js-nolint
new Int32Array()
new Int32Array(length)
new Int32Array(typedArray)
new Int32Array(object)

new Int32Array(buffer)
new Int32Array(buffer, byteOffset)
new Int32Array(buffer, byteOffset, length)
```

> **Note:** `Int32Array()`는 오직 [`new`](/ko/docs/Web/JavaScript/Reference/Operators/new)로만 생성할 수 있습니다. `new` 없이 호출을 시도하면 {{jsxref("TypeError")}} 예외가 발생합니다.

### 매개변수

[`TypedArray`](/ko/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#parameters)를 참고하세요.

### 예외

[`TypedArray`](/ko/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#exceptions)를 참고하세요.

## 예제

### Int32Array을 생성하기 위한 각기 다른 여러 방법

```js
// 길이로부터 생성
const int32 = new Int32Array(2);
int32[0] = 42;
console.log(int32[0]); // 42
console.log(int32.length); // 2
console.log(int32.BYTES_PER_ELEMENT); // 4

// 배열로부터
const x = new Int32Array([21, 31]);
console.log(x[1]); // 31

// 다른 TypedArray로부터
const y = new Int32Array(x);
console.log(y[0]); // 21

// ArrayBuffer로부터
const buffer = new ArrayBuffer(32);
const z = new Int32Array(buffer, 4, 4);
console.log(z.byteOffset); // 4

// 순회로부터
const iterable = (function* () {
  yield* [1, 2, 3];
})();
const int32FromIterable = new Int32Array(iterable);
console.log(int32FromIterable);
// Int32Array [1, 2, 3]
```

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- [`core-js`에서 `Int32Array` 폴리필](https://github.com/zloirock/core-js#ecmascript-typed-arrays)
- [JavaScript 형식화 배열](/ko/docs/Web/JavaScript/Guide/Typed_arrays)
- {{jsxref("ArrayBuffer")}}
- {{jsxref("DataView")}}
