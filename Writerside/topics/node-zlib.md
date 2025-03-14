---
switcher-label: Imports
---

# Zlib

API support and documentation for the `node:zlib`.

<tldr>
    <p>Modules: <code>node:zlib</code></p>
    <p>Support: <img style="inline" src="https://img.shields.io/badge/-alpha-blue" /></p>
    <p>Docs: <a href="https://nodejs.org/api/zlib.html">Node.js Zlib Docs</a></p>
</tldr>

<code-block lang="javascript" switcher-key="ESM">import zlib from "node:zlib"</code-block>
<code-block lang="javascript" switcher-key="CJS">const zlib = require("node:zlib")</code-block>

## Modules

| Status                  | Module             | Docs                                     |
|-------------------------|--------------------|------------------------------------------|
| 🟡 Partially supported. | `node:zlib`        | [Zlib](https://nodejs.org/api/zlib.html) |

## `zlib` | Classes

[`Options`](https://nodejs.org/docs/latest/api/zlib.html#class-options)
: 🟡 Supported, but options are not applied yet.

[`BrotliOptions`](https://nodejs.org/docs/latest/api/zlib.html#class-brotlioptions)
: 🟡 Supported, but options are not applied yet.

[`BrotliCompress`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibbrotlicompress)
: 🟢 Supported.

[`BrotliDecompress`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibbrotlidecompress)
: 🟢 Supported.

[`Deflate`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibdeflate)
: 🟢 Supported.

[`DeflateRaw`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibdeflateraw)
: 🔴 Not implemented.

[`Gunzip`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibgunzip)
: 🟢 Supported.

[`Gzip`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibgzip)
: 🟢 Supported.

[`Inflate`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibinflate)
: 🟢 Supported.

[`InflateRaw`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibinflateraw)
: 🔴 Not implemented.

[`Unzip`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibunzip)
: 🟢 Supported.

[`ZlibBase`](https://nodejs.org/docs/latest/api/zlib.html#class-zlibzlibbase)
: 🔴 Not implemented.

## `zlib` | Properties

[`constants`](https://nodejs.org/docs/latest/api/zlib.html#zlibconstants)
: 🟢 Supported.

## `zlib` | Methods

[`crc32(data[, value])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcrc32data-value)
: 🟢 Supported.

### Streams

These methods create streams which compress or decompress data.

[`createBrotliCompress([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreatebrotlicompressoptions)
: 🟢 Supported.

[`createBrotliDecompress([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreatebrotlidecompressoptions)
: 🟢 Supported.

[`createDeflate([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreatedeflateoptions)
: 🟢 Supported.

[`createDeflateRaw([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreatedeflaterawoptions)
: 🔴 Not implemented.

[`createGunzip([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreategunzipoptions)
: 🟢 Supported.

[`createGzip([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreategzipoptions)
: 🟢 Supported.

[`createInflate([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreateinflateoptions)
: 🟢 Supported.

[`createInflateRaw([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreateinflaterawoptions)
: 🔴 Not implemented.

[`createUnzip([options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibcreateunzipoptions)
: 🟢 Supported.

### Convenience

These methods compress or decompress data.

[`brotliCompress(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibbrotlicompressbuffer-options-callback)
: 🟢 Supported.

[`brotliCompressSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibbrotlicompresssyncbuffer-options)
: 🟢 Supported.

[`brotliDecompress(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibbrotlidecompressbuffer-options-callback)
: 🟢 Supported.

[`brotliDecompressSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibbrotlidecompresssyncbuffer-options)
: 🟢 Supported.

[`deflate(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibdeflatebuffer-options-callback)
: 🟢 Supported.

[`deflateSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibdeflatesyncbuffer-options)
: 🟢 Supported.

[`deflateRaw(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibdeflaterawbuffer-options-callback)
: 🔴 Not implemented.

[`deflateRawSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibdeflaterawsyncbuffer-options)
: 🔴 Not implemented.

[`gunzip(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibgunzipbuffer-options-callback)
: 🟢 Supported.

[`gunzipSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibgunzipsyncbuffer-options)
: 🟢 Supported.

[`gzip(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibgzipbuffer-options-callback)
: 🟢 Supported.

[`gzipSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibgzipsyncbuffer-options)
: 🟢 Supported.

[`inflate(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibinflatebuffer-options-callback)
: 🟢 Supported.

[`inflateSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibinflatesyncbuffer-options)
: 🟢 Supported.

[`inflateRaw(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibinflaterawbuffer-options-callback)
: 🔴 Not implemented.

[`inflateRawSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibinflaterawsyncbuffer-options)
: 🔴 Not implemented.

[`unzip(buffer[, options], callback)`](https://nodejs.org/docs/latest/api/zlib.html#zlibunzipbuffer-options-callback)
: 🟢 Supported.

[`unzipSync(buffer[, options])`](https://nodejs.org/docs/latest/api/zlib.html#zlibunzipsyncbuffer-options)
: 🟢 Supported.
