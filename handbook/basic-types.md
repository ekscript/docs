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

| Length | Signed | Unsigned |
| :--- | :--- | :--- |
| 8-bit | `i8` | `u8` |
| 16-bit | `i16` | `u16` |
| 32-bit | `i32` **\(default\)** | `u32` |

For **Floating-point numbers**, which are numbers with decimal points, EkScript has two types: `f32` and `f64` . On modern CPUs `f64` gives more precision. The _default_ type for floating-point numbers is `f64`

{% tabs %}
{% tab title="TypeScript" %}
```typescript
let decimal: f64 = 6.0;
let anyNumber: number = 6.0;   // number is an alias for f64
let hex: i32 = 0xf00d;
let binary: u8 = 0b1010;
let octal: i32 = 00744;
let separate: i32 = 100_11;
let big: bigint = 100n;
let byte: u8 = b'A'; // u8 only
```
{% endtab %}
{% endtabs %}



#### Type-Coercion

The default type for integer based values is `i32` and for floating point values is `f64`. If during any operation, EkScript is unable to get the number format of any of the variable, it will first try to resort to `i32` and then if nothing is possible to `f64`.

```typescript
let a = 1;  // i32
let b = 1.0; // f64
let c: u8 = 2;

let sum = 1 + 2; // i32
let finalSum = 1 + 2 / 1.5; // f64 (1.0 + 2.0/1.5 = 2.3333..)
let anotherSum: i32 = 1 + 2/1.5; // i32
console.log(anoter)
```

## String

You can use both `'` and `"` quotes for Strings although the default is `'` single quote \(Saving you from using the extra `Shift` key😉\). String behave similar to JavaScript. The compiler will decide if it has to denote a String to byte or not. The developer can use strings without worry though.

```typescript
let color: stinrg = 'blue';
let color = 'red';
```

#### Template strings

You can also use Template strings, spanning multiple lines. These strings are surrounded by the backtick/backquote\(`````\) character. Embedded expressions are of the  `${expr}`.

```typescript
let fullName: string = `Bob Bobbington`;
let age: i32 = 27;
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



