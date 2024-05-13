# Getting Started

Run your first code samples with %product%

## Before you start

You'll need an installed copy of %product%. Follow the [Installation](Installation.md) guide to obtain a copy of
%product%.

## Running some code

%product% can accept a raw string of code or a file to run in any supported language. Best attempts are made to detect
the [primary language](Execution.md#primary-language) via the source file's extension (`.js` will load a JS VM, `.py` a
Python VM, etc.).

1. Let's run a snippet of [JavaScript](JavaScript.md)

   ```bash
    elide run --javascript -c "console.log('Hello!');"
   ```
   ```Console
   Hello!
   Exiting session. Have a great day! 👋
   ```

2. Now let's do the same thing, but with some [Python](Python.md)

   ```bash
    elide run --python -c 'print("Hello!")'
   ```
   ```Console
   Hello!
   Exiting session. Have a great day! 👋
   ```

3. Now let's do the same thing, but with some [Ruby](Ruby.md)

   ```bash
    elide run --ruby -c 'puts "Hello!"'
   ```
   ```Console
   Hello!
   Exiting session. Have a great day! 👋
   ```

> **Language Selection**
>
> %product% can run multiple languages at once. Your primary language selection only affects how your entrypoint script
> is processed; you can run an entrypoint in Python that uses code in JavaScript, for example.
>
{style="note"}

## Polyglot terminal

%product% can run an interactive read-eval-print-loop (REPL) session for each supported language. There are several ways
to kick one off, the easiest being:

**Open a JavaScript console:**
```Console
elide
```

**Open a Python console:**
```Console
elide python
```

**Open a Ruby console:**
```Console
elide ruby
```

> **Exiting the REPL**
>
> You can use <shortcut>Ctrl+D</shortcut> or <shortcut>Ctrl+C</shortcut> twice to exit the interactive session.
>
{style="note"}
