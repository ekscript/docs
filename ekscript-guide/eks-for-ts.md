---
description: "Know TypeScript? It will take about 5 minutes  to get to know what is \U0001F680"
---

# Eks for TS Devs

EkScript is very, very similar to TypeScript. It has the same NodeJS APIs for server-side programming.

### Love Videos 📽 ?

{% hint style="warning" %}
WORK-IN-PROGRESS
{% endhint %}

## Language specification

### No more \`===\`!

rBAAaas



### No \`any\`, \`undefined\`, \`unknown\`, \`never\`, \`NaN\` and false-y values

To maintain a consistent strict code style, EkScript bars you from using `any` , `undefined` , `unknown` , `NaN` and `never` `null` is to be used everywhere wherever previously you used `undefined`. This brings us to the concept of `nullable` and `non-nullable` types. Types that might have a `null` value or might not.

There are no false-y values either. That means `if` statements only take boolean. This also means that `!` unary operator is only for boolean types. Yes, you have to write more code but this will save time in the long run!

```typescript
// --- ❌ ERROR! TS Only ❌ ---

let a = null;    // ❌No Type declaration here

let b: string  = 'Hello'  ; 
b = null; // ❌Non-nullable type

let c = { hello: 'world' }; 
c.hello = null;

let d: undefined;    // ERROR! No type named as undefined

if (a) {}   // ❌ a is not boolean
if (!!c.hello) {} // ❌ a is not boolean

// --- ✅ VALID! Eks ✅ ---
let d: string? = 'Hello';
d = null;    // nullable type

if (d == null) {}

let a = 0;
if (a == 0) {}

type TC = { hello: string?, key: i32 }; // [key: string] : i32
let c = { hello: 'world' };
c.hello = null;    // nullable fields

function fn(a: object) {
    console.log(a?.hello);    // null
}
```

### No return and \`void\` returns

In EkScript you can avoid writing `return` at the end of a function. Just omit \`;\` at the end of the line and boom.

```typescript
function fn(a: f64): f64 {
    let aMod = a + 1.0
    aMod            // returns aMod. Don't use `;`
}
function fn2(b: i32) {
    console.log(`b is : ${b}`)
    // returns void
}

function fn3(c: i32): number {
    return void;    //    explicitly write void
    
    // ❌ no post-return statements
    console.log('Hello World')    // ❌
}
```

## Browser DOM APIs

 EkScript comes with `libDOM.d.eks` which is similar to `libDOM.d.ts` with a more strict API. TypeScript programmers won't even have to sweat on EkScript.

### No Prototype, different \`this\`!

No more 2 ways of defining classes. EkScript is a modern language. It only supports ECMAScript classes. Everything about classes is similar to TypeScript!

This also means that `this` is no longer relevant in functions! Only in classes, `this` is supported. Finally!

```typescript
// --- ❌ ERROR! ❌ ---
Number.prototype.toExponential.call(1);
function f() {
    this.hello = 1;
    this.world = 2
}
f.prototype.hello = 3;
this.hello = 'there';
```

### JSON + JSON5

In TypeScript, `JSON.parse` returns `any` type. EkScript doesn't have `any` . You have to either explicitly infer the type through the generic or by giving the declaration variable the Type

```typescript
type THello = { hello: string } 

// --- ✅ VALID! ✅ ---
const var1 = JSON.parse<THello>('{ "hello": "world" }');
const var2: THello = JSON.parse('{ "hello": "world" }');
const var3 = JSON.parse('{ "hello": "world" }') as THello;

// --- ERROR! ❌ ---
const var3 = JSON.parse('{ "hello": "world" }'); // ❌
someRandomFunc(JSON.parse('{ "hello": "world" }')); // ❌
```

### 

