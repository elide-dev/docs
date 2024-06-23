# Encoding API

Elide supports the standard JavaScript types [`TextEncoder`](#textencoder) and [`TextDecoder`](#textdecoder). These
classes can be used to obtain byte-arrays of strings in different encodings, or to obtain strings from byte arrays with
different encodings.

## Supported Encodings

Elide supports several encodings via the `TextEncoder` and `TextDecoder` constructors:

| Support               | Charset          | Encoding (Label) | Notes            |
|-----------------------|------------------|------------------|------------------|
| 🟢 Supported.         | `ISO_8859_1`     | `iso-8859-1`     |                  |
| 🟢 Supported.         | `ASCII`          | `ascii`          |                  |
| 🟢 Supported.         | `UTF_8`          | `utf-8`          | Default encoding |
| 🔴 Not supported yet. | `UTF_16`         | `utf-16`         |                  |
| 🔴 Not supported yet. | `UTF_32`         | `utf-32`         |                  |
| 🔴 Not supported yet. | (Other charsets) |                  |                  |

## Classes

[`TextEncoder`](#textencoder) Encode strings into byte array representations
: 🟢 Supported.

[`TextDecoder`](#textdecoder) Decode byte arrays into string representations
: 🟢 Supported.

## `TextEncoder`

```Javascript
// create an encoder; by default, it uses utf-8
const encoder = new TextEncoder();
encoder.encoding         // returns 'utf-8'
encoder.encode("hello")  // returns `Uint8Array([...])`
```

The `TextEncoder` class behaves very similarly to how it behaves in a browser, or under Node.js; the only difference is
that Elide supports additional encodings, on top of the default, which is `utf-8`.

> Read more about [`TextEncoder` on MDN](https://developer.mozilla.org/en-US/docs/Web/API/TextEncoder)

### `TextEncoder` Properties

[`TextEncoder.encoding`](https://developer.mozilla.org/en-US/docs/Web/API/TextEncoder/encoding)
: 🟢 Supported.

### `TextEncoder` Methods

[`TextEncoder.encode`](https://developer.mozilla.org/en-US/docs/Web/API/TextEncoder/encode)
: 🟢 Supported.

[`TextEncoder.encodeInto`](https://developer.mozilla.org/en-US/docs/Web/API/TextEncoder/encodeInto)
: 🟢 Supported.

## `TextDecoder`

```Javascript
// create a decoder; by default, it uses utf-8
const decoder = new TextDecoder();
decoder.encoding         // returns 'utf-8'
const input = new Uint8Array([104, 101, 108, 108, 111]);
decoder.decode(input)  // returns 'hello'
```

The `TextDecoder` class behaves identically to how it behaves in a browser, or under Node.js.

> Read more about [`TextDecoder` on MDN](https://developer.mozilla.org/en-US/docs/Web/API/TextDecoder)

### `TextDecoder` Properties

[`TextDecoder.encoding`](https://developer.mozilla.org/en-US/docs/Web/API/TextDecoder/encoding)
: 🟢 Supported.

### `TextDecoder` Methods

[`TextDecoder.decode`](https://developer.mozilla.org/en-US/docs/Web/API/TextDecoder/decode)
: 🟢 Supported.
