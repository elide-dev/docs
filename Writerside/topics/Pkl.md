# Pkl

Pkl is a typed configuration and data language by Apple.
From [Pkl's User Manual](https://pkl-lang.org/main/current/index.html):

> Pkl—pronounced Pickle—is an embeddable configuration language which provides rich support for data templating and
> validation. It can be used from the command line, integrated in a build pipeline, or embedded in a program. Pkl scales
> from small to large, simple to complex, ad-hoc to repetitive configuration tasks.
{style="note"}

---

## What Pkl is for

Pkl allows developers to express structured configurations in a concise and typed dialect (that's Pkl), which can be
rendered into things like JSON, YAML, TOML, and more.

Pkl can also generate code in various languages to interface with these definitions.

<video src="https://www.youtube.com/watch?v=lAxXWYAIt4k" />

> Theo explains why Apple's Pkl language is awesome.

### Why %product% supports Pkl

Have you ever gotten totally lost writing Kubernetes YAMLs, or perhaps been forced to push to GitHub repeatedly until
your CI jobs stop choking on syntax?

Pkl is an end-to-end answer for this problem, and many others. By allowing developers to express data models, or even
actual data, in a typed and concise meta-format, JSON and other formats become checkable, interchangeable, formattable,
and gain many other desirable attributes.

## Usage

%product% integrates with Pkl in several ways:

### Command-line Pkl

The entirety of [Pkl's command line](https://pkl-lang.org/main/current/pkl-cli/index.html) is embedded and supported
within %product%; you can find it at `%cli% pkl`:

```text
Usage: elide pkl [OPTIONS] COMMAND [ARGS]...

Options:
  -v, --version  Show the version and exit
  -h, --help     Show this message and exit

Commands:
  eval              Render pkl module(s)
  repl              Start a REPL session
  test              Run tests within the given module(s)
  project           Run commands related to projects
  download-package  Download package(s)
  analyze           Commands related to static analysis
```

For example, to render Pkl's own [CircleCI configuration](https://github.com/apple/pkl/blob/main/.circleci/config.pkl)
into YAML:

```console
> elide pkl eval ./pkl/.circleci/config.pkl | head -n4

# Generated from CircleCI.pkl. DO NOT EDIT.
version: '2.1'
orbs:
  pr-approval: apple/pr-approval@0.1.0
```
