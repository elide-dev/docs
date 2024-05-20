# Compatibility

%product% is **alpha-quality software**, meaning it has not yet reached a level of stability where correct operation is
guaranteed or even typical.

The language engines used by %product% are based on [GraalVM](https://graalvm.org)
[Truffle](https://www.graalvm.org/latest/graalvm-as-a-platform/language-implementation-framework/). Truffle engines
aren't necessarily compatible by default with their corresponding regular language engines.

Refer to the table below for resources regarding compatibility in each language.

| Language                       | Stability                                                          | %product%'s Engine                                                      | Stock Engine                                   | Notes                                                                                                           |
|--------------------------------|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [JavaScript](JavaScript.md)    | ![Beta](https://img.shields.io/badge/-beta-purple)                 | [GraalJs](https://github.com/oracle/graaljs)                            | [V8](https://v8.dev/)                          | ECMA2023-compatible. [Node API](Node-API.md) compat pending.                                                    |
| [WebAssembly](Experimental.md) | ![Alpha](https://img.shields.io/badge/-alpha-blue)                 | [GraalWasm](https://github.com/oracle/graal/blob/master/wasm/README.md) | [V8](https://v8.dev/)                          |                                                                                                                 |
| [Python](Python.md)            | ![Alpha](https://img.shields.io/badge/-alpha-blue)                 | [GraalPython](https://github.com/oracle/graalpython)                    | [CPython](https://github.com/python/cpython)   | Roughly **~48% compatible** with PyPI top 500. See [here](https://www.graalvm.org/python/compatibility/).       |
| [Ruby](Ruby.md)                | ![Alpha](https://img.shields.io/badge/-alpha-blue)                 | [TruffleRuby](https://github.com/oracle/truffleruby)                    | [MRI](https://rvm.io/interpreters/ruby)        | Passes ~**97% of `ruby/spec`**. See [here](https://www.graalvm.org/latest/reference-manual/ruby/Compatibility/) |
| [LLVM](Experimental.md)        | ![Experimental](https://img.shields.io/badge/-experimental-orange) | [Sulong](https://github.com/oracle/graal/tree/master/sulong)            | [LLVM Runtime](https://llvm.org/)              |                                                                                                                 |
| [TypesScript](TypeScript.md)   | ![Experimental](https://img.shields.io/badge/-experimental-orange) | [TSC](https://github.com/microsoft/typescript)                          | [TSC](https://github.com/microsoft/typescript) |                                                                                                                 |
| [Pkl](Pkl.md)                  | ![Experimental](https://img.shields.io/badge/-experimental-orange) | [Apple Pkl](https://github.com/apple/pkl)                               | [Apple Pkl](https://github.com/apple/pkl)      |                                                                                                                 |
