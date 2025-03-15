---
switcher-label: Imports
---

# Child Process

API support and documentation for the `node:child_process` module.

<tldr>
    <p>Module: <code>node:child_process</code></p>
    <p>Support: <img style="inline" src="https://img.shields.io/badge/-alpha-blue" alt="alpha" /></p>
    <p>Docs: <a href="https://nodejs.org/api/child_process.html">Node.js Child Process Docs</a></p>
</tldr>

<code-block lang="javascript" switcher-key="ESM">import proc from "node:child_process"</code-block>
<code-block lang="javascript" switcher-key="CJS">const proc = require("node:child_process")</code-block>

## Modules

| Status                  | Module                        | Docs                                                                          |
|-------------------------|-------------------------------|-------------------------------------------------------------------------------|
| 🟡 Partially supported. | `node:child_process`          | [Node.js Child Process](https://nodejs.org/api/child_process.html)            |

## `child_process` | Classes

[`ChildProcess`](https://nodejs.org/api/child_process.html#class-childprocess)
: 🟡 Partially supported.

### `ChildProcess` - Events

[`'close'`](https://nodejs.org/api/child_process.html#event-close)
: 🔴 Not implemented.

[`'disconnect'`](https://nodejs.org/api/child_process.html#event-disconnect)
: 🔴 Not implemented.

[`'error'`](https://nodejs.org/api/child_process.html#event-error)
: 🔴 Not implemented.

[`'exit'`](https://nodejs.org/api/child_process.html#event-exit)
: 🔴 Not implemented.

[`'message'`](https://nodejs.org/api/child_process.html#event-message)
: 🔴 Not implemented.

[`'spawn'`](https://nodejs.org/api/child_process.html#event-spawn)
: 🔴 Not implemented.

### `ChildProcess` - Properties

[`channel`](https://nodejs.org/api/child_process.html#subprocesschannel)
: 🔴 Not implemented.

[`connected`](https://nodejs.org/api/child_process.html#subprocessconnected)
: 🟢 Supported.

[`exitCode`](https://nodejs.org/api/child_process.html#subprocessexitcode)
: 🟢 Supported.

[`killed`](https://nodejs.org/api/child_process.html#subprocesskilled)
: 🔴 Not implemented.

[`pid`](https://nodejs.org/api/child_process.html#subprocesspid)
: 🟢 Supported.

[`signalCode`](https://nodejs.org/api/child_process.html#subprocesssignalcode)
: 🔴 Not implemented.

[`spawnargs`](https://nodejs.org/api/child_process.html#subprocessspawnargs)
: 🔴 Not implemented.

[`spawnfile`](https://nodejs.org/api/child_process.html#subprocessspawnfile)
: 🔴 Not implemented.

[`stdin`](https://nodejs.org/api/child_process.html#subprocesssstdin)
: 🟢 Supported.

[`stderr`](https://nodejs.org/api/child_process.html#subprocessstderr)
: 🟢 Supported.

[`stdio`](https://nodejs.org/api/child_process.html#subprocessstdio)
: 🟢 Supported.

[`stdout`](https://nodejs.org/api/child_process.html#subprocessstdout)
: 🟢 Supported.

### `ChildProcess` - Methods

[`disconnect()`](https://nodejs.org/api/child_process.html#subprocessdisconnect)
: 🔴 Not implemented.

[`kill([signal])`](https://nodejs.org/api/child_process.html#subprocesskillsignal)
: 🟢 Supported.

[`[Symbol.dispose]()`](https://nodejs.org/api/child_process.html#subprocesssymboldispose)
: 🔴 Not implemented.

[`ref()`](https://nodejs.org/api/child_process.html#subprocessref)
: 🔴 Not implemented.

[`subprocess.send(message[, sendHandle[, options]][, callback])`](https://nodejs.org/api/child_process.html#subprocesssendmessage-sendhandle-options-callback)
: 🔴 Not implemented.

[`unref()`](https://nodejs.org/api/child_process.html#subprocessunref)
: 🔴 Not implemented.

## `child_process` | Methods

API support is available for spawning child processes **synchronously** or **asynchronously**; refer to the
corresponding section below for your desired call style.

### Process Creation (Asynchronous)

[`exec(command[, options][, callback])`](https://nodejs.org/api/child_process.html#child_processexeccommand-options-callback)
: 🟢 Supported.

[`execFile(file[, args][, options][, callback])`](https://nodejs.org/api/child_process.html#child_processexecfilefile-args-options-callback)
: 🟢 Supported.

[`fork(modulePath[, args][, options])`](https://nodejs.org/api/child_process.html#child_processforkmodulepath-args-options)
: 🔴 Not implemented.

[`spawn(command[, args][, options])`](https://nodejs.org/api/child_process.html#child_processspawncommand-args-options)
: 🟢 Supported.

### Process Creation (Synchronous)

[`execFileSync(file[, args][, options])`](https://nodejs.org/api/child_process.html#child_processexecfilesyncfile-args-options)
: 🟢 Supported.

[`execSync(command[, options])`](https://nodejs.org/api/child_process.html#child_processexecsynccommand-options)
: 🟢 Supported.

[`spawnSync(command[, args][, options])`](https://nodejs.org/api/child_process.html#child_processspawnsynccommand-args-options)
: 🟢 Supported.
