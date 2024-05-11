# Intro: Env Variables

Reading environment variables from JavaScript and Python

> This exercise is part of the [Polyglot 101](Polyglot.md) intro guide.

Many applications use [environment variables](https://en.wikipedia.org/wiki/Environment_variable) to pass small bits of
data between invocations, or across process boundaries.

As part of %product%'s job in unifying multiple languages for use in one program, environment variable access is made
uniform across all languages:

- **Environment is subject to policy.** By default, code **cannot see system environment variables** in %product%; this
  is a big difference with other runtimes, so it bears repeating below.

- **Environment is loaded uniformly.** Support for features like
  [dotenv files](https://stackoverflow.com/questions/68267862/what-is-an-env-or-dotenv-file-exactly) is cross-language
  in Elide. If you see a variable in JavaScript, you will see it as well in Python, Ruby, and so on.

> With %product%, system environment variables are **invisible by default** to running code. You can allow access to
> system variables using [command line flags](CLI-Reference.md).
> {style="note"}

## Before you start

Before running the code below, you'll need to make sure the following is true:

- [%product% is installed](Installation.md)
- The `elide` binary is executable
- The `elide` binary is on your `PATH`, or otherwise referenced in absolute form

## Reading environment variables

We're going to try out %product%'s policies with regard to **reading host environment variables.**

1. Start an interactive session; %product% defaults to JavaScript, so you should get a JavaScript prompt:

   ```bash
    export ELIDE_TESTING="hello"
    elide repl
    elide (js) >
   ```

   > Use `Ctrl+C` twice or `Ctrl+D` to exit the interactive session.

2. %product% provides the [`process`](https://nodejs.org/api/process.html#process) object, just like Node:

   ```bash
   elide (js) > process.env.ELIDE_TESTING
   undefined
   ```
   
   Our `ELIDE_TESTING` environment variable isn't showing up! That's because %product% forbids access to environment
   variables by default.

3. Now, let's run the REPL session again, but with access to host environment:
   
   ```bash
   elide repl --allow:host-env
   elide (js) > process.env.ELIDE_TESTING
   hello
   ```

   Neat! We can see the environment variable.

4. Now let's try Python:

   ```Python
   elide repl --python
   elide (python) > import os; os.environ
   Environ(ELIDE_INTERNAL, ELIDE_ROOT, NODE_ENV)
   ```
   
   > %product% provides the `NODE_ENV` variable to all languages, set to either `'development'` or `'production'`.

5. And with environment access enabled:

   ```Python
   elide repl --python --allow:host-env
   elide (python) > import os; os.environ
   Environ(ANDROID_HOME, AWS_ACCESS_KEY_ID, ... ELIDE_TESTING, ...)
   ```

   Of course, the accessing variable returns the expected value:

   ```Python
   elide repl --python --allow:host-env
   elide (python) > import os; os.environ["ELIDE_TESTING"]
   'hello'
   ```

## What you've learned {id="what-learned"}

In this tutorial, you learned about %product%'s policy enforcement around env variable access, and how it interoperates
with JavaScript and Python.

<seealso>
    <category ref="tutorialSeries">
        <a href="Polyglot.md">Back to Polyglot 101</a>
        <a href="101-Filesystem.md">Next exercise: Filesystem access</a>
    </category>
</seealso>
