---
switcher-label: Imports
---

# Assertions

API support and documentation for the `node:assert` module.

<tldr>
    <p>Module: <code>node:assert</code></p>
    <p>Support: <img style="inline" src="https://img.shields.io/badge/-beta-purple" /></p>
    <p>Docs: <a href="https://nodejs.org/api/assert.html">Node.js Assertion Docs</a></p>
</tldr>

<code-block lang="javascript" switcher-key="ESM">import assert from "node:assert"</code-block>
<code-block lang="javascript" switcher-key="CJS">const assert = require("node:assert")</code-block>

## Modules

| Status                  | Module               | Docs                                                                          | Notes                   |
|-------------------------|----------------------|-------------------------------------------------------------------------------|-------------------------|
| 🟢 Supported.           | `node:assert`        | [Assertions](https://nodejs.org/api/assert.html)                              | Standard assertions.    |
| 🔴 Not yet implemented. | `node:assert/strict` | [Strict Assertions](https://nodejs.org/api/assert.html#strict-assertion-mode) | Strict-mode assertions. |

## `assert` | Classes

[`AssertionError`](https://nodejs.org/api/assert.html#new-assertassertionerroroptions)
: 🟢 Supported.

[`CallTracker`](https://nodejs.org/api/assert.html#new-assertassertionerroroptions)
: 🔴 Not implemented; deprecated at Node.js v20.

## `assert` | Methods

[`assert(value[, message])`](https://nodejs.org/api/assert.html#assertvalue-message)
: 🟡 Implemented; awaiting bugfix for default module exports. Use `assert.ok()` in the meantime.

[`assert.deepEqual(actual, expected[, message])`](https://nodejs.org/api/assert.html#assertdeepequalactual-expected-message)
: 🔴 Not yet implemented.

[`assert.deepStrictEqual(actual, expected[, message])`](https://nodejs.org/api/assert.html#assertdeepstrictequalactual-expected-message)
: 🔴 Not yet implemented.

[`assert.doesNotMatch(string, regexp[, message])`](https://nodejs.org/api/assert.html#assertdoesnotmatchstring-regexp-message)
: 🟢 Supported.

[`assert.doesNotReject(asyncFn[, error][, message])`](https://nodejs.org/api/assert.html#assertdoesnotrejectasyncfn-error-message)
: 🟢 Supported.

[`assert.doesNotThrow(fn[, error][, message])`](https://nodejs.org/api/assert.html#assertdoesnotthrowfn-error-message)
: 🟢 Supported.

[`assert.equal(actual, expected[, message])`](https://nodejs.org/api/assert.html#assertequalactual-expected-message)
: 🟢 Supported.

[`assert.fail([message])`](https://nodejs.org/api/assert.html#assertfailmessage)
: 🟢 Supported.

[`assert.fail(actual, expected[, message[, operator[, stackStartFn]]])`](https://nodejs.org/api/assert.html#assertfailactual-expected-message-operator-stackstartfn)
: 🟢 Supported.

[`assert.ifError(value)`](https://nodejs.org/api/assert.html#assertiferrorvalue)
: 🟢 Supported.

[`assert.match(string, regexp[, message])`](https://nodejs.org/api/assert.html#assertmatchstring-regexp-message)
: 🟢 Supported.

[`assert.notDeepEqual(actual, expected[, message])`](https://nodejs.org/api/assert.html#assertnotdeepequalactual-expected-message)
: 🔴 Not yet implemented.

[`assert.notDeepEqualStrict(actual, expected[, message])`](https://nodejs.org/api/assert.html#assertnotdeepequalstrictactual-expected-message)
: 🔴 Not yet implemented.

[`assert.notEqual(actual, expected[, message])`](https://nodejs.org/api/assert.html#assertnotequalactual-expected-message)
: 🟢 Supported.

[`assert.notStrictEqual(actual, expected[, message])`](https://nodejs.org/api/assert.html#assertnotstrictequalactual-expected-message)
: 🔴 Not yet implemented.

[`assert.ok(value[, message])`](https://nodejs.org/api/assert.html#assertokvalue-message)
: 🟢 Supported.

[`assert.rejects(asyncFn[, error][, message])`](https://nodejs.org/api/assert.html#assertrejectsasyncfn-error-message)
: 🟢 Supported.

[`assert.strictEqual(actual, expected[, message])`](https://nodejs.org/api/assert.html#assertstrictequalactual-expected-message)
: 🔴 Not yet implemented.

[`assert.throws(fn[, error][, message])`](https://nodejs.org/api/assert.html#assertthrowsfn-error-message)
: 🟢 Supported.
