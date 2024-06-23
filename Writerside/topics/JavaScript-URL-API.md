# URL API

Elide supports the [WhatWG](https://whatwg.org) [URL API Specification](https://url.spec.whatwg.org/); this is the spec
you use when you use the global `URL` class in JavaScript.

Elide's implementation of `URL` and `URLSearchParams` are based on JDK 22's
[`URI`](https://docs.oracle.com/en%2Fjava%2Fjavase%2F22%2Fdocs%2Fapi%2F%2F/java.base/java/net/URI.html),
[`URL`](https://docs.oracle.com/en%2Fjava%2Fjavase%2F22%2Fdocs%2Fapi%2F%2F/java.base/java/net/URL.html),
and
[`URLDecoder`](https://docs.oracle.com/en%2Fjava%2Fjavase%2F22%2Fdocs%2Fapi%2F%2F/java.base/java/net/URLDecoder.html)
classes.

## Classes

[`URL`](#url) Parse and manipulate URLs
: 🟢 Supported.

[`URLSearchParams`](#urlsearchparams) Parse and manipulate URL params
: 🟢 Supported.

## `URL`

```Javascript
const url = new URL('https://google.com/search')
url.pathname  // returns '/search'
url.hostname  // returns 'google.com'
```

> Read more about the standard JavaScript `URL` class [on MDN](https://developer.mozilla.org/en-US/docs/Web/API/URL)

The `URL` class is used as a [value class](https://en.wikipedia.org/wiki/Value_object) which wraps a standard
[Uniform Resource Locator](https://en.wikipedia.org/wiki/URL), also known as a "URL". URLs have a specific structure and
suite of supported components, as opposed to their more general ancestor,
[URIs](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier).

URLs are strictly validated: when you construct one from a string, it is parsed eagerly, and you will get an error if
the provided string is not a valid URL.

URLs, by spec, support the following components:

| `URL` Property                                                                      | Sample Value                                 | Description                                                                                |
|-------------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------|
| [`protocol`](https://developer.mozilla.org/en-US/docs/Web/API/URL/protocol)         | `'https:'`                                   | The transport technology in use, including the trailing `:`; usually `http:` or `https:`   |
| [`origin`](https://developer.mozilla.org/en-US/docs/Web/API/URL/origin)             | `'https://google.com:443'`                   | The web origin value of the URL; consists of the scheme, domain, and port                  |
| [`host`](https://developer.mozilla.org/en-US/docs/Web/API/URL/host)                 | `'google.com:443'`                           | The full host string, like `https://google.com:443` from the example above                 |
| [`hostname`](https://developer.mozilla.org/en-US/docs/Web/API/URL/hostname)         | `'google.com'`                               | Just the hostname, like `google.com` from the sample above                                 |
| [`port`](https://developer.mozilla.org/en-US/docs/Web/API/URL/port)                 | `443`                                        | Just the port, like `443` from the sample above (HTTPS)                                    |
| [`pathname`](https://developer.mozilla.org/en-US/docs/Web/API/URL/pathname)         | `/search`                                    | The path portion of the url `/like-this/here`, or `/` at a minimum                         |
| [`hash`](https://developer.mozilla.org/en-US/docs/Web/API/URL/hash)                 | `#hello`                                     | The portion of the URL after `#`, if present                                               |
| [`href`](https://developer.mozilla.org/en-US/docs/Web/API/URL/href)                 | `'https://google.com/search'`                | Formatted string version of the whole URL                                                  |
| [`username`](https://developer.mozilla.org/en-US/docs/Web/API/URL/username)         | `'user'`                                     | If there is auth information in the URL (like `user:pass@...`), this is `user`             |
| [`password`](https://developer.mozilla.org/en-US/docs/Web/API/URL/password)         | `'pass'`                                     | `password`: If there is auth information in the URL (like `user:pass@...`), this is `pass` |
| [`search`](https://developer.mozilla.org/en-US/docs/Web/API/URL/search)             | `'?hello=hi'`                                | The portion of the URL after `?` but before `#`, if present, including the initial `?`     |
| [`searchParams`](https://developer.mozilla.org/en-US/docs/Web/API/URL/searchParams) | [`URLSearchParams`](#urlsearchparams) object | Parsed `search` value into a multimap of key-value pairs                                   |

## `URLSearchParams`

Coming soon.
