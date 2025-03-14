# README

<img src="elide-marquee.png" alt="%product%" />

[%product%](https://elide.dev) is a high-performance multi-language software runtime. Here you can find reference docs, guides,
code samples, and more.

<br />

🚀 **%product% is a runtime, like Node or Python.**

You install it on your machine as a standalone binary. %product% is
statically linked and has essentially zero runtime dependencies.

You can install it on macOS or Linux with this one-liner:
<br />
<code-block lang="bash">curl -sSL --tlsv1.2 elide.sh | bash -s -</code-block>

🗺️ **%product% can run multiple languages.**

JavaScript, TypeScript, WASM, and Python are built-in. Ruby, JVM (Java,
Kotlin, Scala), and LLVM (Swift, C++, Rust) are on the way.

<code-block lang="typescript">
// hello.ts
import { sayHello } from "./my-app.py"

// this line exists to show that this is typescript lol
const msg: string = () => `${sayHello()} + TypeScript!`
console.log(JSON.stringify({x: msg()}))
</code-block>

<code-block lang="python">
# my-app.py
def say_hello():
  """Render a greeting."""
  return f"Hello from Python"
</code-block>

<code-block lang="Console" prompt=">">
elide ./hello.ts
</code-block>

<code-block lang="Console">
{"x": "Hello from Python + TypeScript!"}
</code-block>

⏫ **%product% is extremely fast.**

- ☑️ %product% runs your Python code **up to 3x faster than CPython**.
- ☑️ %product% runs your TypeScript code **faster than Node can run JavaScript**.
- ☑️ %product% runs your HTTP endpoints at up to **800,000 requests per second**.

> %product% is independently benchmarked by TechEmpower. [Latest results][2]
{style="note"}

🧘 **%product% supports the APIs you already know and the tools you already love.**

- ☑️ %product% is [WinterTC][3] compatible.
- ☑️ Like other JS runtimes, %product% **supports a large slice of the [Node API](Node-API.md)**.
- ☑️ Works with **NPM and PyPI**, **CJS** and **ESM**.
- ☑️ Insanely fast **dependency installation** (via [orogene][0] and [uv][1]).

## %product% is in beta

Check out %product%'s launch video

<video src="https://youtu.be/Txl9ryfbCw4" preview-src="launch-cover.png" />

<br />

<seealso style="cards">
    <category ref="gettingStarted">
        <a summary="Install %product% on your machine" href="Installation.md">Installing %product%</a>
        <a summary="Code samples in each language" href="GettingStarted.md">Getting Started</a>
        <a summary="Thinking about software in more than one language" href="Polyglot.md">Polyglot 101: Thinking in Multiple Languages</a>
        <a summary="Runtime usage guides by language" href="Language-Guides.topic">%product% Runtime: Language Guides</a>
    </category>
</seealso>

[0]: https://orogene.dev/
[1]: https://github.com/astral-sh/uv
[2]: https://www.techempower.com/benchmarks/#hw=ph&test=plaintext&section=data-r23:~:text=133-,elide,-4%2C089%2C078
[3]: https://wintertc.org
