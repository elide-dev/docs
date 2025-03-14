# Architecture

%product% is powered by several insanely cool technologies. In no particular order:

- **[GraalVM][0] is %product%'s main execution engine** and guest interpreter/compiler. %product% leverages [Truffle][1]
  language engines, including [GraalJs][2], [GraalPython][3], [TruffleRuby][4], and [Sulong][5].

- Most of %product% is **written in [Kotlin][7]** and built against the [JVM 23][8]. Thus, %product%'s own code is
  checked extensively at build-time for `null` safety, and is memory-safe by default.

- Native portions of %product% are **written in [Rust][9]**, which extends safety guarantees as much as possible even
  outside the context of the JVM/SVM.

- Networking in %product% is **powered by [Netty][10]**, which offers world-class performance and durability for
  networked applications.

- %product% embeds **best-of-breed tooling** for guest languages: [oxc][11], [orogene][12], and [uv][13] are available
  transparently. **[Pkl is supported][14] for configuration** and interoperable data expression.

- **[Micronaut][6] wires together %product%** internally, with build-time dependency injection (DI). This architecture
  is what keeps startup time fast while preserving modularity.

## Specific topics

Read more about:

- **[](Security.md)**
- **[](Performance.md)**

## How %product% works

<img src="arch-v1.svg" />

> Note: This is already out of date, but it's as close as we have right now to an architectural diagram.

[0]: https://graalvm.org
[1]: https://www.graalvm.org/latest/graalvm-as-a-platform/language-implementation-framework/
[2]: https://github.com/oracle/graaljs
[3]: https://github.com/oracle/graalpython
[4]: https://github.com/oracle/truffleruby
[5]: https://github.com/oracle/graal/blob/master/sulong/README.md
[6]: https://micronaut.io
[7]: https://kotlinlang.org
[8]: https://en.wikipedia.org/wiki/Java_virtual_machine
[9]: https://rustlang.org
[10]: https://netty.io/
[11]: https://oxc.rs
[12]: https://orogene.dev
[13]: https://github.com/astral-sh/uv
[14]: https://pkl-lang.org
