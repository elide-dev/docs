# Polyglot 101

Traditionally, software is written in **just one language** at a time: there are JavaScript apps, and
Python scripts, and all sorts of other things developers make.

%product% offers a new way to think about software: in **multiple languages at once** (hence, "polyglot!"). But what
does that mean? This guide explains how multiple languages can work in tandem to accomplish amazing things.

## Starting Imperatively

Let's start with a simple imperative example of how multiple languages might work together. We could begin with some
JavaScript:

```Javascript
export function sayHello(name) {
  console.log(`Hello, ${name}!`);
}
```

We've defined a function here, which takes a `name` parameter; we format that and print it. Easy. Now let's imagine our
magic runtime can shift to Python to call that code:

```Python
from "./my-js.mjs" import sayHello as say_hello

def call_hello():
  """Call the `sayHello` function in JavaScript, from Python."""
  say_hello("%product%")
```

This is pretty easy to follow so far. We've defined that `sayHello` function in JavaScript, and now we are calling that
same function from a new function, called `callHello`, in Python.

## But why?

Have you ever wanted to write a Python app which could host a React UI? How about an application that's built in Ruby;
maybe you want to do some image processing and you miss your PIL?

There are tons of cases where one language is good at something, another is good at something else, and your app has to
do both. %product% is what bridges this gap.

## Isn't that inefficient?

That depends! %product% certainly behaves differently from, say, Node, but %product% handily beats Node and even Bun on
several key benchmarks. Just like Bun vs. Node, or CPython vs. PyPy, performance isn't necessarily apples-to-apples.

But, since you may be wondering, in the code sample above 👆

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

```Javascript
export function sayHello(nameGetter) {
  console.log(`Hello, ${nameGetter()}!`);
}
```

And:

```Python
from "./my-js.mjs" import sayHelloWithGetter as say_hello

def get_name():
  return "Elide"

def call_hello_look_ma_try_this_with_serialization():
  say_hello(get_name)
```

%product% will happily run this code. This is impossible with JSON, or Protobuf, or any other trickery on top of Node.js
or CPython.

> %product% is up to **3x faster than CPython**, **22x faster than CRuby**, and **75x faster than Node v20**, even with
> cross-language calling overhead.
> {style="note"}

## Let's do some exercises

Now that we are thinking in a roughly-polyglot way, let's test the waters with some basics: many applications have to
**read environment variables** or **write to a file**. You can follow the guides below or skip ahead.

[Exercise: Environment Variables](101-Environment.md)
: Read env variables and use %product%'s host policy to restrict host env access

[Exercise: Filesystem Basics](101-Filesystem.md)
: Read a file using Node.js built-ins ([`node:fs`](https://nodejs.org/api/fs.html)).

## Benchmarking

%product% makes use of language runtimes from the [GraalVM](https://graalvm.org) team which are benchmarked extensively
and continuously. People often ask if they can replicate these benchmarks. The answer is yes, you are encouraged to!

There are some tools we can recommend:

| Tool                                                | Great for                      | Example invocation                                                    |
|-----------------------------------------------------|--------------------------------|-----------------------------------------------------------------------|
| [`hyperfine`](https://github.com/sharkdp/hyperfine) | CLI-invocable micro-benchmarks | [Using Hyperfine for benchmarks](#benchmarking-with-hyperfine)        |
| [`wrk2`]( https://github.com/giltene/wrk2)          | Server benchmarking            | [Using wrk2 to benchmark %product%'s server](#benchmarking-with-wrk2) |

### Benchmarking with Hyperfine

Coming soon.

### Benchmarking with wrk2

Coming soon.
