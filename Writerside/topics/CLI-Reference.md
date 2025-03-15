# CLI Reference

%product% supports multiple sub-commands, similar to Git.

## Usage

Syntax:

```text
 Usage:
    or:  elide info|help|discord|bug... [OPTIONS]
    or:  elide srcfile.<js|ts|...> [OPTIONS]
    or:  elide js|node|deno [OPTIONS] [FILE] [ARG...]
    or:  elide js|node|deno [OPTIONS] [--code CODE]
    or:  elide run|repl|serve [OPTIONS] [FILE] [ARG...]
    or:  elide run|repl|serve [OPTIONS] [--code CODE]
    or:  elide run|repl [OPTIONS]
    or:  elide run|repl --js [OPTIONS]
    or:  elide run|repl --language=[JS] [OPTIONS] [FILE] [ARG...]
    or:  elide run|repl --languages=[JS,PYTHON,...] [OPTIONS] [FILE] [ARG...]

Manage, configure, and run polyglot applications with Elide

Parameters:
      [FILE]      Source file to run.
      [ARG...]    Arguments to pass

Options:
  -h, --help      Show this message and exit.
  -V, --version   Print version information and exit.

Commands:
  info                 Show info about the current app and environment
  help, bug, issue
                       Report an issue or bug, find help for using Elide
  run, r, serve, repl
                       Run a polyglot script, server, or interactive shell
  pkl
                       Run the Pkl command-line tools
  discord              Open or show a Discord invite link

Exit Codes:
  0   Successful program execution.
  1    Generic failure (terminal).
  2    Exception in user code.
```

## Runner Commands

`run`, `r`, `repl`
: Run a script file or a snippet of code; if no code is given, start an interactive REPL session. %product% will select
an appropriate language if given a clearly identifiable source file (Python for `.py`, Ruby for `.rb`, etc.).

`serve`
: Alias to `run` a server in any language; %product% will block until the server exits.

`python`
: Alias to `run` some Python. Equivalent to `elide run --python ...`.

`ruby`
: Alias to `run` some Ruby. Equivalent to `elide run --ruby ...`.

`js`
: Runs a file. Equivalent to `elide run --javascript ...`. Note that JavaScript is the default language engine.

## Utility Commands

`install`
: Install dependencies for an %product% project; this includes all supported ecosystems by default.

`info`
: Show info about the current installation of %product%.

`discord`
: Open an invite to %product%'s Discord server.

`help`
: Show documentation on various topics.

`bug`, `issue`
: File an issue or a feature request for %product%.

## Global Options

Describe what each option is used for:

-h, --help
: Show help text for any command.

-v, --version
: Show the installed version of %product% and exit.

--verbose
: Activate verbose logging.

-d, --debug
: Activate debug logging. **Caution:** Debug-level logging can be very verbose.
