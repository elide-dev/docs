
# Elide Documentation

> [!TIP]
> See the main [docs site](https://docs.elide.dev) to actually read the docs

This project is compatible with [JetBrains Writerside](https://www.jetbrains.com/writerside/), an IDE for technical writing and documentation. The outputs
of this project combine with [Dokka](https://github.com/Kotlin/dokka) and [Knit](https://github.com/Kotlin/kotlinx-knit) content to create Elide's [documentation site](https://docs.elide.dev).

## Project Structure

Documentation structure is described using a combination of XML and Markdown; XML is used to describe categories and
hierarchy, and Markdown/[MDX](https://mdxjs.com/) is used to describe actual content. This project focuses on
**narrative documentation**, where Dokka focuses on API docs, and Knit focuses on code samples.

### API Docs

API documentation is generated for each release of Elide, and included as an archive in the [API directory](./API). This content is merged with the main doc site content on-build, and it is published in unison.

## Contributing

There isn't a contributor guide yet, but you can get started by cloning the repo and opening it in Writerside. You can also refer to the contributor guide in the main [Elide repo](https://github.com/elide-dev/elide).

