# TypeScript

%product% can run [TypeScript][0] directly, without a build step; TypeScript is parsed natively via [OXC][1], and then
executed via the built-in [JavaScript engine](JavaScript.md).

```Console
elide ./script.{ts,cts,mts}
```
```JavaScript
// from typescript, javascript
import { x, y, z } from "./script.{ts,cts,mts}"

// cjs and esm are supported
const { x, y, z } = require("./script.{ts,cts,mts}")
```

## Language Engine

%product% can execute TypeScript under the following conditions.

| -------- | ---------------------------------------------------- |
| Language | **TypeScript**                                       |
| Standard | `5.8.x`                                              |
| Maturity | ![Beta](https://img.shields.io/badge/-beta-purple)   |
| Engine   | [GraalJs](https://github.com/oracle/graaljs) + [OXC](https://oxc.rs)               |

## How to use it

1) **%product% can execute TypeScript directly.** Just pass a TypeScript file (CJS or ESM) to `elide` or `elide run`;
   anytime the JavaScript engine is active, the TypeScript layer is active too.

2) **%product% can import TypeScript directly.** When running JavaScript or other languages like Python, imports treat
   TypeScript files as transparently-compiled JavaScript, and default to ESM. Importing a TypeScript file from JS
   behaves identically as JS; importing from Python produces an object of exports.

3) **%product% can transparently compile JSX and TSX.** *SX code is transparently compiled as it is interpreted by the
   runtime, same as vanilla TypeScript.

> JSX and TSX are not yet available in %product%'s command-line.
{style="warn"}

## How it works

%product% parses TypeScript directly with [OXC][1]'s high-performance native parser, in Rust, and then interprets the
code as normal on top of the JavaScript engine. Bindings that need to be present for features like JSX are injected into
the JavaScript context transparently.

This "type-stripping" pre-compiling step takes very little time: on the order of milliseconds, and is amortized over all
runs for a given TypeScript source root, since %product% aggressively caches ASTs at the bytecode stage.

As a result, TypeScript execution is often nearly cost-free compared to regular JavaScript:

![bench-js-vs-ts.png](bench-js-vs-ts.png)

> Executing a non-trivial JavaScript sample vs. an identical TypeScript sample.
{style="note"}

<img src="oxc-parsing.svg" width="600" alt="OXC parsing speed compared to SWC and Biome: it's the fastest" />

> Parsing speed comparison from OXC's own benchmarks.
{style="note"}

[0]: https://www.typescriptlang.org/
[1]: https://oxc.rs
