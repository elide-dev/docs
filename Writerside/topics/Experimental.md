# Experimental Engines

%product% has experimental support for **JVM**, **LLVM**, and **WebAssembly.** These engines are still under
construction upstream, as part of [GraalVM](https://graalvm.org).

| **Engine**  | **Implementation**                                                           | **Status**                                                                               |
|-------------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| JVM         | [Espresso](https://www.graalvm.org/latest/reference-manual/java-on-truffle/) | ![Experimental](https://img.shields.io/badge/-experimental-orange) **Linux amd64 only.** |
| LLVM        | [Sulong](https://www.graalvm.org/latest/reference-manual/llvm/)              | ![Experimental](https://img.shields.io/badge/-experimental-orange)                       |
| WebAssembly | [GraalWasm](https://www.graalvm.org/latest/reference-manual/wasm/)           | ![Experimental](https://img.shields.io/badge/-experimental-orange)                       |
| Pkl         | [Apple Pkl](https://github.com/apple/pkl)                                    | ![Experimental](https://img.shields.io/badge/-experimental-orange)                       |

Several experimental engines support multiple dialects.

| Language    | Engine | Status                                                                                                        |
|-------------|--------|---------------------------------------------------------------------------------------------------------------|
| Java        | JVM    | ![Experimental](https://img.shields.io/badge/-experimental-orange)  **Linux amd64 only.** Not yet documented. |
| Kotlin      | JVM    | ![Experimental](https://img.shields.io/badge/-experimental-orange)  **Linux amd64 only.** Not yet documented. |
| Groovy      | JVM    | Not yet available.                                                                                            |
| Scala       | JVM    | Not yet available.                                                                                            |
| C/C++       | LLVM   | Not yet available.                                                                                            |
| Rust        | LLVM   | Not yet available.                                                                                            |
| Swift       | LLVM   | Not yet available.                                                                                            |
| Bitcode     | LLVM   | ![Experimental](https://img.shields.io/badge/-experimental-orange)  **Linux amd64 only.** Not yet documented. |
| WebAssembly | WASM   | ![Experimental](https://img.shields.io/badge/-experimental-orange)  Not yet documented.                       |
