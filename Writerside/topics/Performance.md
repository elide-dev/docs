# Performance

%product% is built on top of [GraalVM][0] and [Truffle][1]. This core difference leads to significant performance
advantages, especially with regard to polyglot programming.

%product% uses GraalVM in place of V8 or JSC (used by Node/Deno and Bun, respectively).

## GraalVM + Truffle

Instead of implementing just one language (V8 implements JavaScript, CPython implements Python, and so on), GraalVM and
Truffle, together, constitute an abstract framework for authoring a high-performance JIT interpreter and compiler.

Languages are simply dialects (Truffle) into this shared backend (Graal). %product% wires together the APIs necessary to
make this into a luxurious experience.

Some notes about why GraalVM + Truffle is so fast:

- **Graal is a state-of-the-art optimizing compiler**, implementing advanced code generation and speculative
  optimization techniques.

- **Graal can see across language borders**, enabling inlining across languages and other compiler tricks. It's all
  "just code" to the Graal compiler, whether it is Python, JavaScript, or something else.

- **Graal can collect garbage across borders**, so pauses are minimized and cohesive.

## Language Performance

Notes about pure language execution performance.

### JavaScript, TypeScript, WASM

%product% is competitive with Node and Deno at execution of [](JavaScript.md), [](TypeScript.md), and
[](WebAssembly.md).

Pure JS/TS startup time for %product% can be very fast:

| Runtime | Language              | Case        | Startup (cold) | Server hit (hot) |
|---------|-----------------------|-------------|----------------|------------------|
| Bun     | JavaScript/TypeScript | Hello World | ~6.5ms         | ~1.5ms           |
| Node    | JavaScript Only       | Hello World | ~10ms          | ~7ms             |
| Deno    | JavaScript Only       | Hello World | ~15ms          | ~71ms            |
| Elide   | JavaScript/TypeScript | Hello World | ~20ms          | ~2ms             |

> Numbers are representative of expected performance on Linux/amd64 with a modern CPU. [TechEmpower][2] independently
> benchmarks %product% (see benchmarks below).
{style="note"}

### Python

%product% is competitive with modern optimizing Python runtimes like PyPy and often beats CPython. GraalPython provides
[continuous benchmarks upstream](https://www.graalvm.org/python/docs/#python-performance).

<img src="graalpy-performance.png" width="600" alt="Geomean speedup over CPython" />

[0]: https://graalvm.org
[1]: https://www.graalvm.org/latest/graalvm-as-a-platform/language-implementation-framework/
[2]: https://www.techempower.com/benchmarks/#hw=ph&test=plaintext&section=data-r23:~:text=0-,elide,-2.4%20ms
