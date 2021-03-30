---
description: TypeScript but more native. More strict. More fun!
---

# EkScript

{% hint style="warning" %}
EkScript implementation is not done. This documentation page only focuses on its specifications
{% endhint %}

![](.gitbook/assets/ekscript.png)

## What is EkScript? 

**EkScript is a strictly-typed subset of TypeScript that compiles to C and JS allowing you to leverage multiple platforms as a target.**

EkScript was built in a way that TypeScript developers can onboard in less than 10 minutes. EkScript won't change much of TypeScript and the JS like ecosystem and ships with a standard library that will be familiar to most JS/TS developers. It strips away unnecessary legacy JavaScript syntax and code and starts afresh taking inspiration from ES2020.

EkScript's C target provides an excellent C ABI and improved memory consumption and performance over NodeJS. Like TypeScript it provides support for browser based applications by simply stripping away the types and producing almost 1-1 JavaScript code without overhead.

### Why EkScript?

EkScript was built out of the need for a programming language that meets the following requirements for an alternative language that...

1. **...is based on another very, very popular language developers use at present.** TypeScript's popularity and similarity with EkScript means developers won't have to relearn everything from scratch.
2. **...has static typing for avoiding runtime errors:** EkScript has a strong typing system making it perfect for minimizing trivial development bugs.
3. **...has the standard library similar to JavaScript:** TypeScript's choice for the base language means that EkScript supports all NodeJS and Browser APIs out-of-the-box. This means developers are jumping into familiar grounds and use their favorite standard library features.
4. **...compiles to 2 most popular programming languages**: EkScript's ability to compile/transpile to JavaScript and C gives it the ability to run on every possible platform present today ranging from the web to small-embedded devices. Its a real **write-once-run-anywhere \(WORA\)** programming language.
5. **...excellent C ABI:** EkScript ships with an excellent C ABI which allows developers to plugin any library written in Rust, C++, C, Zig to provide a overheadless EkScript front-end. Further compilation to C means EkScript is faster and consumes less memory than NodeJS
6. **...pattern matching:** The only addition to EkScript is its pattern matching syntax which takes inspiration from many functional programming languages. This paves the way for Types as first class citizens of the language.

And many more things.

## What's inside?

### **EkScript** ❤️ **TypeScript**

All TypeScript modules are 100% compatible with EkScript through an easy-to-use interop. So, no more wasting time relearning new languages.

To get how EkScript differs from TypeScript: 

{% page-ref page="ekscript-guide/eks-for-ts.md" %}

### **EkScript Bundler**

EkScript comes with a modern bundler that takes care of all the difficult configurations for you.

## Let's get started then!







