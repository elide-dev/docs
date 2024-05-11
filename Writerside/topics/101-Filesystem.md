# Intro: Filesystem

Filesystem access with %product%

> This exercise is part of the [Polyglot 101](Polyglot.md) intro guide.

Coming soon.

> Like [env variables](101-Environment.md), %product% **isolates filesystem I/O by default**; unless you grant
> permission, code running under %product% (in any language) cannot see your disk.
> {style="note"}

## Before you start

Before running the code below, you'll need to make sure the following is true:

- [%product% is installed](Installation.md)
- The `elide` binary is executable
- The `elide` binary is on your `PATH`, or otherwise referenced in absolute form

## Reading files from disk

We're going to try out %product%'s isolation with regard to **disk I/O**

1. Start an interactive session. %product% starts you with JavaScript. Let's also create a file which we will read:

   ```bash
    echo "testing" > hello.txt
    elide repl
    elide (js) >
   ```

   > Use `Ctrl+C` twice or `Ctrl+D` to exit the interactive session.

2. Now, let's import the [`node:fs`](https://nodejs.org/api/fs.html) module:

   ```bash
   elide (js) > const fs = require('node:fs');
   ```
   
   > %product% aims for full Node API support, but we aren't there yet. See the [Node API reference](Node-API.md).

3. Let's read the file we just wrote:
   
   ```bash
   elide (js) > fs.readFileSync("hello.txt", {encoding: 'utf-8'})
   testing
   ```

   Neat! We can read the file.
