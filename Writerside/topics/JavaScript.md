# JavaScript

%product% can execute JavaScript, just like Node.js, Deno, or Bun. Similar to other popular JavaScript runtimes,
%product% strives for Node API compatibility.

```Console
elide run --javascript ...
```
```Javascript
export default function hello() {
  console.log("Elide can run JavaScript!")
}
```

## Language Engine

%product% is an ECMA2023-compliant JavaScript engine. JS is the most mature language offered by %product%; execution is
powered by [GraalJs](https://github.com/oracle/graaljs), which ships with GraalVM.

| Language | **JavaScript**                                     |
|----------|----------------------------------------------------|
| Standard | ECMA2024                                           |
| Maturity | ![Beta](https://img.shields.io/badge/-beta-purple) |
| Engine   | [GraalJs](https://github.com/oracle/graaljs)       |

## Standards Conformance

Elide conforms to several JavaScript standards:

### WinterTC

Elide is a [WinterTC](https://wintertc.org)-conforming runtime; Elide supports the [Minimum Common API][0] and several
other WinterTC proposals or standards.

See our [WinterTC Conformance](WinterTC.md) page for more information.

### Node API

The [Node API](https://nodejs.org/api) constitutes the functions and modules provided by Node.js on top of V8; the Node
API is quite large and covers everything from assertion testing to zlib compression.

%product% aims for full Node API compatibility _where possible and applicable._ What does that mean? Well, %product% is
written on top of [GraalVM](https://graalvm.org) rather than V8, so immediately several Node API modules do not apply
(for example, the `v8` module).

Most Node.js applications and libraries only make use of a small surface area of the Node API. As [Bun](https://bun.sh)
and [Deno](https://deno.land) have shown, a great deal of software can run out of the box with sufficient
(but incomplete) Node API coverage.

> See Elide's [Node API reference](Node-API.md) for more information.

## Performance

Elide executes JavaScript with comparable performance to V8-based runtimes like Node and Deno, and JSC runtimes like
Bun. Although GraalVM is a completely different core engine, it is well suited for CLI and server use, whereas V8 and
JSC were architected with browsers in mind.

As a result, Elide can deliver very strong performance in JavaScript, especially for server-side use cases.

**[Elide is ranked highly on the TechEmpower benchmarks.][1]** At the time of this writing Elide holds the
**133rd position** for plaintext responses. Node & Deno, FastAPI & Django (Python), and many other popular frameworks
rank lower than this score.

| **Tech stack**     | **TechEmpower Rank** | Typical RPS (🔼 is better) | Warm hit latency (🔽 is better) | Cold start latency (🔽 is better) |
|--------------------|----------------------|----------------------------|---------------------------------|-----------------------------------|
| Elide + JavaScript | 133                  | ~800,000+                  | ~3ms                            | ~30ms                             |
| Deno               | 184                  | ~200,000                   | ~70ms                           | ~15ms                             |
| Node.js + Express  | 364                  |                            | ~550ms                          | ~10ms                             |
| FastAPI + Python   | 292                  |                            | ~30ms                           |                                   |
| Django + Python    | 388                  |                            | ~65ms                           |                                   |
| Node.js + Next.js  | 497                  | ~3,000                     | ~700ms                          |                                   |

> All scores are selected from the _first_ (highest performing) benchmark for a given framework. All numbers shown were
> measured on modern `Linux x86-64`.

## Glossary

JavaScript
: It's a software language I suppose.

Node.js
: It's a JavaScript runtime which is designed primarily for server-side use. Node.js embeds Google's V8 JavaScript
engine, the same available in Google Chrome.

Node API
: Suite of APIs provided on top of regular JavaScript, which, collectively, become Node.js. For example, if you're ever
imported or required the `fs` or `path` module, you've used the Node API.

ECMAScript
: Formal name for JavaScript, as defined by the ECMAScript Standard. JavaScript language versions are denoted as ECMA
years; for example, 'ECMA2023' includes JavaScript features up to the year 2023.

<seealso style="cards">
    <category ref="gettingStarted">
        <a summary="Node API support in %product%" href="Node-API.md">Node API support</a>
        <a summary="Running TypeScript apps in %product%" href="TypeScript.md">TypeScript</a>
    </category>
</seealso>

[0]: https://min-common-api.proposal.wintertc.org/
[1]: https://www.techempower.com/benchmarks/#hw=ph&test=plaintext&section=data-r23
