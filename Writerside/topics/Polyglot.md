# Polyglot 101

Traditionally, software is written in **just one language** at a time: there are JavaScript apps, and
Python scripts, and all sorts of other things developers make.

%product% offers a new way to think about software: in **multiple languages at once** (hence, "polyglot!"). But what
does that mean? This guide explains how multiple languages can work in tandem to accomplish amazing things.

## Starting Imperatively

Let's start with a simple imperative example of how multiple languages might work together. We could begin with some
Python:

```Python
# sample.py

def say_hello(name = "Python"):
  """Say hello to someone or something."""
  return f"Hello, {name}!"
```

Now let's save that file and create a new one. This time, in TypeScript:

```TypeScript
// sample.ts
import py from "./sample.py"

console.log(`${py.say_hello()} + TypeScript!`)
```

We've defined some code in Python, and now we are **importing it into TypeScript**. This code is runnable with Elide:

```Console
> elide sample.ts
```
```Console
Hello, Python + TypeScript!
```

## But why?

Have you ever wanted to write a Python app which could host a React UI?

There are tons of cases where one language is good at something, another is good at something else, and your app has to
do both. %product% is what bridges this gap.

## Isn't that inefficient?

%product% outperforms Node, Deno, _and_ CPython. But, since you may be wondering, in the code sample above 👆

- **There is just one process.** No, %product% isn't calling out to Node with your source code, and then to Python, and
  stitching between with JSON or something. That _would_ be gross. There are systems that do this; Elide is not one
  of them.

- **There is just one governing interpreter.** %product% uses language implementations from the
  [GraalVM](https://graalvm.org) team, built on top of
  [Truffle](https://www.graalvm.org/latest/graalvm-as-a-platform/language-implementation-framework/). Instead of two
  interpreters (Python and JavaScript, in this case), there's just one, but it _speaks both languages_.

- **There is no serialization going on.** The `name` value doesn't need to be transformed as it crosses a border between
  Python and JavaScript. It's just a string; both languages can use it as they would normally.

Skeptical? Good. The best engineers often are. Let's beat the serialization allegations:

```Python
# sample.py

def say_hello(name_getter):
  return f"Hello, {name_getter()}!"

def say_goodbye(name_getter):
  return f"Goodbye, {name_getter()}!"

def render_message(leaving = False):
  if leaving: return say_goodbye
  return say_hello
```

And:

```TypeScript
// sample.ts
import py from "./sample.py"

const helloName = () => "Elide"
const goodbyeName = () => "confining runtimes"

console.log(
  // will render a hello message, passing functions between langs
  py.render_message()(helloName)
)
console.log(
  // will render a goodbye message
  py.render_message(true)(goodbyeName)
)
```

```Console
> elide sample.ts
```
```Console
Hello, Elide!
Goodbye, confining runtimes!
```

%product% will happily run this code. This is impossible with JSON, or Protobuf, or any other trickery on top of Node.js
or CPython.

> %product% is up to **3x faster than CPython**, **22x faster than CRuby**, and **75x faster than Node v20**, even with
> cross-language calling overhead.
> {style="note"}

When people see a demo like this, the "polyglot" concept immediately begins to make sense. That's great, but how do 2+
languages interact in one context?

## Let's do some exercises

Now that we are thinking in a roughly-polyglot way, let's test the waters with some basics: many applications have to
**read environment variables** or **write to a file**. You can follow the guides below or skip ahead.

[Exercise: Environment Variables](101-Environment.md)
: Read env variables and use %product%'s host policy to restrict host env access

[Exercise: Filesystem Basics](101-Filesystem.md)
: Read a file using Node.js built-ins ([`node:fs`](https://nodejs.org/api/fs.html)).

[Exercise: Debugging](101-Debugging.md)
: Step across language boundaries in a debugger

[Exercise: Interop](101-Polyglot-Context.md)
: Get familiar with cross-lang interop

[Exercise: Servers](101-Servers.md)
: Writing polyglot servers with %product%

## Benchmarking

%product% makes use of language runtimes from the [GraalVM](https://graalvm.org) team which are benchmarked extensively
and continuously. People often ask if they can replicate these benchmarks. The answer is yes, you are encouraged to!

There are some tools we can recommend:

| Tool                                                | Great for                      |
|-----------------------------------------------------|--------------------------------|
| [`hyperfine`](https://github.com/sharkdp/hyperfine) | CLI-invocable micro-benchmarks |
| [`wrk2`]( https://github.com/giltene/wrk2)          | Server benchmarking            |

Read more about %product%'s [](Performance.md)
