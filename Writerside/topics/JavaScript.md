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
| Standard | ECMA2023                                           |
| Maturity | ![Beta](https://img.shields.io/badge/-beta-purple) |
| Engine   | [GraalJs](https://github.com/oracle/graaljs)       |

## Node API

The [Node API](https://nodejs.org/api) constitutes the functions and modules provided by Node.js on top of V8; the Node
API is really big, and covers everything from assertion testing to zlib compression.

%product% aims for full Node API compatibility _where possible and applicable._ What does that mean? Well, %product% is
written on top of [GraalVM](https://graalvm.org) rather than V8, so immediately several Node API modules do not apply
(for example, the `v8` module).

Most Node.js applications and libraries only make use of a small surface area of the Node API. As [Bun](https://bun.sh)
and [Deno](https://deno.land) have shown, a great deal of software can run out of the box with sufficient
(but incomplete) Node API coverage.

> See Elide's [Node API reference](Node-API.md) for more information.

## Performance

Coming soon.

## Stability

Coming soon.

## Glossary

A definition list or a glossary:

JavaScript
: It's a software language... barely.

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
