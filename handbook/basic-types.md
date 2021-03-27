---
description: EkScript has all the TypeScript basic types with special additions
---

# Basic Types

## Boolean

Most basic type. Has only two values: `true` and `false` . Denoted by `boolean`

```typescript
let isDone: boolean = false
```

## Numbers

This is one of those places where EkScript is different from TypeScript. EkScript supports a wide variety of numbers, including `bigint` . You can also `_` as a visual separator such as `1_000` . You can declare types from any of the following **integer**  types:

| Length | Signed |
| :--- | :--- |
| 8-bit | char |
| 32-bit | int |
| 64-bit | `float` |

{% tabs %}
{% tab title="TypeScript" %}
```typescript
let decimal: float = 6.0;
let anyNumber: number = 6.0;   // number is an alias for float
let hex: int = 0xf00d;
let binary: int = 0b1010;
let octal: int = 00744;
let separate: int = 100_11;
let big: bigint = 100n;
let byte: char = 'A'; // u8 only
```
{% endtab %}
{% endtabs %}

You also have `bigint`

#### Type-Coercion

The default type for integer based values is `int` and for floating point values is `float`. 

```typescript
let a = 1;  // i32
let b = 1.0; // f64
let c: int = 2;

let sum = 1 + 2; // i32
let finalSum = 1 + 2 / 1.5; // f64 (1.0 + 2.0/1.5 = 2.3333..)
let anotherSum: int = 1 + 2/1.5; // i32
console.log(anoter)
```

## String

You can use both `'` and `"` quotes for Strings although the default is `'` single quote. String behave similar to JavaScript. The developer can use strings without worry though.

```typescript
let color: string = 'blue';
let color = 'red';
```

#### Template strings

You can also use Template strings, spanning multiple lines. These strings are surrounded by the backtick/backquote\(`````\) character. Embedded expressions are of the  `${expr}`.

```typescript
let fullName: string = `Bob Bobbington`;
let age: int = 27;
let sentence = `Hello, my name is ${fullName}.
And my age is ${age}
`;
```

The above `sentence` variable is equivalent to:

```typescript
let sentence: string = 'Hello, my name is '
    + fullName
    + '.\n\n'
    + 'I\'ll be'
    + (age + 1)
    + ' years old next month';
```



