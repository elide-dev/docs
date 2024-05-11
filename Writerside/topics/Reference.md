# Reference

Use this section to find reference docs which describe APIs, command line flags, and other detailed behavior in
%product%.

## Command Line

Use this reference to determine flags and subcommands for the `elide` binary.

```bash
elide
```
```text
Usage:
  or:  elide info|help|discord|bug... [OPTIONS]
  or:  elide srcfile.<js|py|rb|kt|java|wasm|...> [OPTIONS]
  or:  elide js|kt|jvm|python|ruby|wasm|node|deno [OPTIONS] [FILE]
  or:  elide run|repl|serve [OPTIONS] [FILE]
  or:  elide run|repl|serve [OPTIONS] [--code CODE]
  or:  elide run|repl [OPTIONS]
  or:  elide run|repl --js [OPTIONS]
  or:  elide run|repl --language=[JS] [OPTIONS] [FILE]
  or:  elide run|repl --languages=[JS,PYTHON,...] [OPTIONS] [FILE]

Manage, configure, and run polyglot applications with Elide
```

- [Full CLI reference](CLI-Reference.md)

## Framework APIs

%product% can also be used as a framework, within a regular JVM application. Artifacts are made available via
Maven Central.

<seealso>
    <category ref="referenceDocs">
        <a href="CLI-Reference.md">CLI reference docs</a>
        <a href="https://docs.elide.dev/apidocs/">Framework API docs</a>
    </category>
</seealso>
