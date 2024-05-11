
# Elide Documentation

> [!TIP]
> See the main [Elide repository](https://github.com/elide-dev/elide) to actually read the docs

This project is compatible with [JetBrains Writerside](https://www.jetbrains.com/writerside/), an IDE for technical writing and documentation. The outputs
of this project combine with [Dokka](https://github.com/Kotlin/dokka) and [Knit](https://github.com/Kotlin/kotlinx-knit) content to create Elide's [documentation site](https://docs.elide.dev).

## Project Structure

Documentation structure is described using a combination of XML and Markdown; XML is used to describe categories and
hierarchy, and Markdown/[MDX](https://mdxjs.com/) is used to describe actual content. This project focuses on
**narrative documentation**, where Dokka focuses on API docs, and Knit focuses on code samples.

This codebase includes docs from [`elide-dev/elide`](https://github.com/elide-dev/elide) through
[Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules). Elide is pinned at a particular commit hash, and
then docs are consumed and included via Writerside and Gradle.

## Contributing

There isn't a contributor guide yet, but you can get started by cloning the repo and opening it in Writerside.
