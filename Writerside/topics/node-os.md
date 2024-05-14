---
switcher-label: Imports
---

# OS

API support and documentation for the `node:os` module.

<tldr>
    <p>Module: <code>node:os</code></p>
    <p>Support: <img style="inline" src="https://img.shields.io/badge/-alpha-blue" /></p>
    <p>Docs: <a href="https://nodejs.org/api/os.html">Node.js OS Docs</a></p>
</tldr>

<code-block lang="javascript" switcher-key="ESM">import os from "node:os"</code-block>
<code-block lang="javascript" switcher-key="CJS">const os = require("node:os")</code-block>

## Modules

| Status                  | Module             | Docs                                         |
|-------------------------|--------------------|----------------------------------------------|
| 🟢 Supported.           | `node:os`          | [Node.js OS](https://nodejs.org/api/os.html) |

## `os` | Properties

[`EOL`](https://nodejs.org/api/os.html#oseol)
: 🟢 Supported.

[`devNull`](https://nodejs.org/api/os.html#osdevnull)
: 🟢 Supported.

## `os` | Methods

[`availableParallelism()`](https://nodejs.org/api/os.html#osavailableparallelism)
: 🟢 Supported.

[`arch()`](https://nodejs.org/api/os.html#osarch)
: 🟢 Supported.

[`cpus()`](https://nodejs.org/api/os.html#oscpus)
: 🟢 Supported.

[`endianness()`](https://nodejs.org/api/os.html#osendianness)
: 🟢 Supported.

[`freemem()`](https://nodejs.org/api/os.html#osfreemem)
: 🟢 Supported.

[`getPriority([pid])`](https://nodejs.org/api/os.html#osgetprioritypid)
: 🔴 Not implemented.

[`homedir()`](https://nodejs.org/api/os.html#oshomedir)
: 🟢 Supported.

[`hostname()`](https://nodejs.org/api/os.html#oshostname)
: 🟢 Supported.

[`loadavg()`](https://nodejs.org/api/os.html#osloadavg)
: 🟢 Supported.

[`machine()`](https://nodejs.org/api/os.html#osmachine)
: 🔴 Not implemented.

[`networkInterfaces()`](https://nodejs.org/api/os.html#osnetworkinterfaces)
: 🟡 Implemented; not yet compliant.

[`platform()`](https://nodejs.org/api/os.html#osplatform)
: 🟢 Supported.

[`release()`](https://nodejs.org/api/os.html#osrelease)
: 🟡 Implemented; not yet compliant.

[`setPriority([pid, ]priority)`](https://nodejs.org/api/os.html#ossetprioritypid-priority)
: 🔴 Not implemented.

[`tmpdir()`](https://nodejs.org/api/os.html#ostmpdir)
: 🟢 Supported.

[`totalmem()`](https://nodejs.org/api/os.html#ostotalmem)
: 🟢 Supported.

[`type()`](https://nodejs.org/api/os.html#ostype)
: 🟢 Supported.

[`uptime()`](https://nodejs.org/api/os.html#osuptime)
: 🟢 Supported.

[`userInfo([options])`](https://nodejs.org/api/os.html#osuserinfooptions)
: 🔴 Not implemented.

[`version()`](https://nodejs.org/api/os.html#osversion)
: 🟡 Implemented; not yet compliant.

--

[`appendFile(path, data[, options], callback)`](https://nodejs.org/api/fs.html#fsappendfilepath-data-options-callback)
: 🔴 Not implemented.

[`readFile(path[, options], callback)`](https://nodejs.org/api/fs.html#fsreadfilepath-options-callback)
: 🟡 Supported for UTF-8 reads. Binary reads do not work yet.
