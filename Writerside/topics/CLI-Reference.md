# CLI Reference

%product% supports multiple sub-commands, similar to Git or Bun.

## Usage

Syntax:

```text
elide [OPTIONS]
  or:  elide info|help|discord|bug... [OPTIONS]
  or:  elide srcfile.<js|py|rb|kt|java|wasm|...> [OPTIONS]
  or:  elide js|kt|jvm|python|ruby|wasm|node|deno [OPTIONS] [FILE]
  or:  elide run|repl|serve [OPTIONS] [FILE]
  or:  elide run|repl|serve [OPTIONS] [--code CODE]
  or:  elide run|repl [OPTIONS]
  or:  elide run|repl --js [OPTIONS]
  or:  elide run|repl --language=[JS] [OPTIONS] [FILE]
  or:  elide run|repl --languages=[JS,PYTHON,...] [OPTIONS] [FILE]
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
: Opens a file. Equivalent to `elide run --javascript ...`. Note that JavaScript is the default language engine.

## Utility Commands

`info`
: Show info about the current installation of %product%.

`discord`
: Open an invite to %product%'s Discord server.

`help`
: Show documentation on various topics.

`bug`, `issue`
: File an issue or a feature request for %product%.

`selfupdate`
: Upgrade %product% to the latest version in-place.

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

<seealso>
    <!--Provide links to related how-to guides, overviews, and tutorials.-->
</seealso>