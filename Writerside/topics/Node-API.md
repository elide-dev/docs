# Node API

Elide aims for near-complete Node.js API compatibility; where modules don't make sense or aren't possible to implement,
problems are noted below.

Most `npm` packages intended for `Node.js` environments will work with Elide out of the box; the best way to know for certain is to try it.

This page is updated regularly to reflect compatibility status of the latest version of Elide.
The information below reflects Elide's's compatibility with _Node.js v22_.

If you run into any bugs with a particular package, please [open an issue](https://github.com/elide-dev/elide/issues/new).
Opening issues for compatibility bugs helps us prioritize what to work on next.

| **API**                  | **Pinned Version** |
|--------------------------|--------------------|
| Node.js Standard Library | Node `v22.0.0`     |

## Legend

- 🔴 Not implemented, can't implement, won't implement; this is not a final state.
- 🟡 In progress, coming soon, under testing/experimental, available but not fully in compliance yet.
- 🟢 Fully implemented; total or near-total compliance.

## Built-in modules

[`node:assert`](node-assert.md)
: 🟢 Supported.

[`node:assert/strict`](node-assert.md)
: 🟡 Coming soon.

[`node:async_hooks`](https://nodejs.org/api/async_hooks.html)
: 🔴 Not implemented.

[`node:buffer`](https://nodejs.org/api/buffer.html)
: 🟡 Partial support.

[`node:child_process`](https://nodejs.org/api/child_process.html)
: 🟡 Partial support.

[`node:cluster`](https://nodejs.org/api/cluster.html)
: 🔴 Not implemented.

[`node:console`](https://nodejs.org/api/console.html)
: 🟡 Coming soon. See [`console`](#globals) global, which is supported.

[`node:crypto`](https://nodejs.org/api/crypto.html)
: 🔴 Not implemented.

[`node:dgram`](https://nodejs.org/api/dgram.html)
: 🔴 Not implemented.

 [`node:diagnostics_channel`](https://nodejs.org/api/diagnostics_channel.html)
: 🔴 Not implemented.

[`node:dns`](https://nodejs.org/api/dns.html)
: 🔴 Not implemented.

[`node:domain`](https://nodejs.org/api/domain.html)
: 🔴 Not implemented.

[`node:events`](node-events.md)
: 🟢 Supported.

[`node:fs`](node-fs.md)
: 🟡 Some methods are implemented (`readFile`, `readFileSync`, `writeFile`, `writeFileSync`, etc.).

[`node:http`](https://nodejs.org/api/http.html)
: 🔴 Not implemented.

[`node:http2`](https://nodejs.org/api/http2.html)
: 🔴 Not implemented.

[`node:https`](https://nodejs.org/api/https.html)
: 🔴 Not implemented.

[`node:inspector`](https://nodejs.org/api/inspector.html)
: 🔴 Not implemented.

[`node:module`](https://nodejs.org/api/module.html)
: 🔴 Not implemented.

[`node:net`](https://nodejs.org/api/net.html)
: 🔴 Not implemented.

[`node:os`](node-os.md)
: 🟢 Supported.

[`node:path`](node-path.md)
: 🟢 Supported.

[`node:perf_hooks`](https://nodejs.org/api/perf_hooks.html)
: 🔴 Not implemented.

[`node:process`](https://nodejs.org/api/process.html)
: 🟢 Supported.

[`node:punycode`](https://nodejs.org/api/punycode.html)
: 🔴 Not implemented.

[`node:querystring`](https://nodejs.org/api/querystring.html)
: 🔴 Not implemented.

[`node:readline`](https://nodejs.org/api/readline.html)
: 🔴 Not implemented.

[`node:repl`](https://nodejs.org/api/repl.html)
: 🔴 Not implemented.

[`node:stream`](https://nodejs.org/api/stream.html)
: 🟢 Supported.

[`node:string_decoder`](https://nodejs.org/api/string_decoder.html)
: 🔴 Not implemented.

[`node:sys`](https://nodejs.org/api/util.html)
: 🟡 See `node:util`.

[`node:test`](https://nodejs.org/api/test.html)
: 🔴 Not implemented.

[`node:timers`](https://nodejs.org/api/timers.html)
: 🔴 Not implemented.

[`node:tls`](https://nodejs.org/api/tls.html)
: 🔴 Not implemented.

[`node:trace_events`](https://nodejs.org/api/tracing.html)
: 🔴 Not implemented.

[`node:tty`](https://nodejs.org/api/tty.html)
: 🔴 Not implemented.

[`node:url`](node-url.md)
: 🟢 Supported.

[`node:util`](https://nodejs.org/api/util.html)
: 🟡 Mostly polyfilled.

[`node:v8`](https://nodejs.org/api/v8.html)
: 🔴 Not implemented.

[`node:vm`](https://nodejs.org/api/vm.html)
: 🔴 Not implemented.

[`node:wasi`](https://nodejs.org/api/wasi.html)
: 🔴 Not implemented.

[`node:worker_threads`](https://nodejs.org/api/worker_threads.html)
: 🔴 Not implemented.

[`node:zlib`](https://nodejs.org/api/zlib.html)
: 🟢 Supported.

## Globals

The table below lists all globals implemented by Node.js and Bun's current compatibility status.

[`AbortController`](https://developer.mozilla.org/en-US/docs/Web/API/AbortController)
: 🟢 Supported.

[`AbortSignal`](https://developer.mozilla.org/en-US/docs/Web/API/AbortSignal)
: 🟢 Supported.

[`Blob`](https://developer.mozilla.org/en-US/docs/Web/API/Blob)
: 🟢 Supported.

[`Buffer`](https://nodejs.org/api/buffer.html#class-buffer)
: 🟢 Supported.

[`ByteLengthQueuingStrategy`](https://developer.mozilla.org/en-US/docs/Web/API/ByteLengthQueuingStrategy)
: 🟢 Supported.

[`__dirname`](https://nodejs.org/api/globals.html#__dirname)
: 🟢 Supported in CJS contexts.

[`__filename`](https://nodejs.org/api/globals.html#__filename)
: 🟢 Supported in CJS contexts.

[`atob()`](https://developer.mozilla.org/en-US/docs/Web/API/atob)
: 🟢 Supported.

[`BroadcastChannel`](https://developer.mozilla.org/en-US/docs/Web/API/BroadcastChannel)
: 🔴 Not implemented.

[`btoa()`](https://developer.mozilla.org/en-US/docs/Web/API/btoa)
: 🟢 Supported.

[`clearImmediate()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/clearImmediate)
: 🟢 Supported.

[`clearInterval()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/clearInterval)
: 🟢 Supported.

[`clearTimeout()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/clearTimeout)
: 🟢 Supported.

[`CompressionStream`](https://developer.mozilla.org/en-US/docs/Web/API/CompressionStream)
: 🔴 Not implemented.

[`console`](https://developer.mozilla.org/en-US/docs/Web/API/console)
: 🟢 Supported.

[`CountQueuingStrategy`](https://developer.mozilla.org/en-US/docs/Web/API/CountQueuingStrategy)
: 🔴 Not implemented.

[`Crypto`](https://developer.mozilla.org/en-US/docs/Web/API/Crypto)
: 🔴 Not implemented.

[`SubtleCrypto (crypto)`](https://developer.mozilla.org/en-US/docs/Web/API/crypto)
: 🔴 Not implemented.

[`CryptoKey`](https://developer.mozilla.org/en-US/docs/Web/API/CryptoKey)
: 🔴 Not implemented.

[`CustomEvent`](https://developer.mozilla.org/en-US/docs/Web/API/CustomEvent)
: 🟢 Supported.

[`DecompressionStream`](https://developer.mozilla.org/en-US/docs/Web/API/DecompressionStream)
: 🔴 Not implemented.

[`Event`](https://developer.mozilla.org/en-US/docs/Web/API/Event)
: 🟢 Supported.

[`EventTarget`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget)
: 🟢 Supported.

[`exports`](https://nodejs.org/api/globals.html#exports)
: 🟢 Supported.

[`fetch`](https://developer.mozilla.org/en-US/docs/Web/API/fetch)
: 🟢 Supported (experimental).

[`FormData`](https://developer.mozilla.org/en-US/docs/Web/API/FormData)
: 🔴 Not implemented.

[`global`](https://nodejs.org/api/globals.html#global)
: 🟢 Aliases to `globalThis`.

[`globalThis`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/globalThis)
: 🟢 Supported. This is an object containing all objects in the global namespace. It's rarely referenced directly, as its contents are available without an additional prefix, e.g. `__dirname` instead of `global.__dirname`.

[`Headers`](https://developer.mozilla.org/en-US/docs/Web/API/Headers)
: 🟢 Supported.

[`MessageChannel`](https://developer.mozilla.org/en-US/docs/Web/API/MessageChannel)
: 🔴 Not implemented.

[`MessageEvent`](https://developer.mozilla.org/en-US/docs/Web/API/MessageEvent)
: 🔴 Not implemented.

[`MessagePort`](https://developer.mozilla.org/en-US/docs/Web/API/MessagePort)
: 🔴 Not implemented.

[`module`](https://nodejs.org/api/globals.html#module)
: 🟢 Supported.

[`PerformanceEntry`](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceEntry)
: 🔴 Not implemented.

[`PerformanceMark`](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceMark)
: 🔴 Not implemented.

[`PerformanceMeasure`](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceMeasure)
: 🔴 Not implemented.

[`PerformanceObserver`](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceObserver)
: 🔴 Not implemented.

[`PerformanceObserverEntryList`](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceObserverEntryList)
: 🔴 Not implemented.

[`PerformanceResourceTiming`](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceResourceTiming)
: 🔴 Not implemented.

[`performance`](https://developer.mozilla.org/en-US/docs/Web/API/performance)
: 🟢 Supported.

[`process`](https://nodejs.org/api/process.html)
: 🟢 Supported.

[`queueMicrotask()`](https://developer.mozilla.org/en-US/docs/Web/API/queueMicrotask)
: 🟢 Supported.

[`ReadableByteStreamController`](https://developer.mozilla.org/en-US/docs/Web/API/ReadableByteStreamController)
: 🟢 Supported.

[`ReadableStream`](https://developer.mozilla.org/en-US/docs/Web/API/ReadableStream)
: 🟢 Supported.

[`ReadableStreamBYOBReader`](https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamBYOBReader)
: 🟢 Supported.

[`ReadableStreamBYOBRequest`](https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamBYOBRequest)
: 🟢 Supported.

[`ReadableStreamDefaultController`](https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamDefaultController)
: 🟢 Supported.

[`ReadableStreamDefaultReader`](https://developer.mozilla.org/en-US/docs/Web/API/ReadableStreamDefaultReader)
: 🟢 Supported.

[`require()`](https://nodejs.org/api/globals.html#require)
: 🟢 Supported, including [`require.main`](https://nodejs.org/api/modules.html#requiremain), [`require.cache`](https://nodejs.org/api/modules.html#requirecache), [`require.resolve`](https://nodejs.org/api/modules.html#requireresolverequest-options)

[`Response`](https://developer.mozilla.org/en-US/docs/Web/API/Response)
: 🟢 Supported.

[`Request`](https://developer.mozilla.org/en-US/docs/Web/API/Request)
: 🟢 Supported.

[`setImmediate()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/setImmediate)
: 🟡 Coming soon.

[`setInterval()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/setInterval)
: 🟢 Supported.

[`setTimeout()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/setTimeout)
: 🟢 Supported.

[`structuredClone()`](https://developer.mozilla.org/en-US/docs/Web/API/structuredClone)
: 🟢 Supported.

[`SubtleCrypto`](https://developer.mozilla.org/en-US/docs/Web/API/SubtleCrypto)
: 🔴 Not implemented.

[`DOMException`](https://developer.mozilla.org/en-US/docs/Web/API/DOMException)
: 🔴 Not implemented.

[`TextDecoder`](https://developer.mozilla.org/en-US/docs/Web/API/TextDecoder)
: 🟢 Supported.

[`TextDecoderStream`](https://developer.mozilla.org/en-US/docs/Web/API/TextDecoderStream)
: 🔴 Not implemented.

[`TextEncoder`](https://developer.mozilla.org/en-US/docs/Web/API/TextEncoder)
: 🟢 Supported.

[`TextEncoderStream`](https://developer.mozilla.org/en-US/docs/Web/API/TextEncoderStream)
: 🔴 Not implemented.

[`TransformStream`](https://developer.mozilla.org/en-US/docs/Web/API/TransformStream)
: 🟢 Supported.

[`TransformStreamDefaultController`](https://developer.mozilla.org/en-US/docs/Web/API/TransformStreamDefaultController)
: 🟢 Supported.

[`URL`](https://developer.mozilla.org/en-US/docs/Web/API/URL)
: 🟢 Supported; approaches full compliance.

[`URLSearchParams`](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams)
: 🟢 Supported.

[`WebAssembly`](https://nodejs.org/api/globals.html#webassembly)
: 🟢 Supported.

[`WritableStream`](https://developer.mozilla.org/en-US/docs/Web/API/WritableStream)
: 🟢 Supported.

[`WritableStreamDefaultController`](https://developer.mozilla.org/en-US/docs/Web/API/WritableStreamDefaultController)
: 🟢 Supported.

[`WritableStreamDefaultWriter`](https://developer.mozilla.org/en-US/docs/Web/API/WritableStreamDefaultWriter)
: 🟢 Supported.

## Let us know what you need

We prioritize upcoming Node API work based on need; please
[file an issue](https://github.com/elide-dev/elide/issues/new) if you see a module you need which isn't implemented.
