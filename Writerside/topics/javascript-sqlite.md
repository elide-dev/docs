---
switcher-label: Imports
---

# SQLite in JavaScript

<tldr>
    <p>Module: <code>elide:sqlite</code></p>
    <p>Support: <img style="inline" src="https://img.shields.io/badge/-beta-purple" /></p>
    <p>Docs: <a href="https://bun.sh/docs/api/sqlite">Bun SQLite Docs</a></p>
</tldr>

Elide embeds native support for [SQLite3](https://sqlite.org), with bindings into JavaScript. The API provided is
identical to [Bun's SQLite bindings](https://bun.sh/docs/api/sqlite).

<code-block lang="javascript" switcher-key="ESM">import { Database } from "elide:sqlite"</code-block>
<code-block lang="javascript" switcher-key="CJS">const { Database } = require("elide:sqlite")</code-block>

```Javascript
import { Database } from "elide:sqlite"
const db = new Database()
db.exec("CREATE TABLE test (id INTEGER PRIMARY KEY, name TEXT);")
db.exec("INSERT INTO test (name) VALUES ('foo');")
db.query("SELECT * FROM test;").get()["name"]
// 'foo'
```

> Bindings are on the way for Python and Ruby.
> {style="note"}

## `sqlite` | Classes

[`Database`](https://bun.sh/docs/api/sqlite#database)
: 🟢 Supported.
