# Assertions

API support and documentation for the `node:assert` module.

<tabs>
    <tab title="ESM">
        <code-block lang="javascript">import assert from "node:assert"</code-block>
    </tab>
    <tab title="CJS">
        <code-block lang="javascript">const assert = require("node:assert")</code-block>
    </tab>
</tabs>

| Specification | Module        | Support                                            | Documentation                                                |
|---------------|---------------|----------------------------------------------------|--------------------------------------------------------------|
| Node.js API   | `node:assert` | ![Beta](https://img.shields.io/badge/-beta-purple) | [Node.js Assertion Docs](https://nodejs.org/api/assert.html) |

## Methods

[`assert(value[, message])`](https://nodejs.org/api/assert.html#assertvalue-message)
: 🟢 Supported. An alias of `assert.ok()`.

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
