---
switcher-label: Imports
---

# URL

API support and documentation for the `node:url` module.

<tldr>
    <p>Module: <code>node:url</code></p>
    <p>Support: <img style="inline" src="https://img.shields.io/badge/-alpha-blue" /></p>
    <p>Docs: <a href="https://nodejs.org/api/url.html">Node.js URL Docs</a></p>
</tldr>

<code-block lang="javascript" switcher-key="ESM">import fs from "node:fs"</code-block>
<code-block lang="javascript" switcher-key="CJS">const fs = require("node:fs")</code-block>
<code-block lang="javascript" switcher-key="ESM">import fs from "node:fs/promises"</code-block>
<code-block lang="javascript" switcher-key="CJS">const fs = require("node:fs/promises")</code-block>

## Modules

| Status         | Module      |
|----------------|-------------|
| 🟢 Supported.  | `node:url`  |

| Standard / Docs                                                  | Notes                                                 |
|------------------------------------------------------------------|-------------------------------------------------------|
| [Node.JS URL API](https://nodejs.org/api/url.html)               | Node's take on the URL standard.                      |
| [WHATWG: URL Standard](https://url.spec.whatwg.org/)             | Universal URL standard offered by WHATWG.             |
| [MDN: URL](https://developer.mozilla.org/en-US/docs/Web/API/URL) | MDN's documentation for the URL standard in browsers. |

## `url` | Classes

[`URL`](https://nodejs.org/api/url.html#class-url)
: 🟢 Supported.

[`URLSearchParams`](https://nodejs.org/api/url.html#class-urlsearchparams)
: 🟢 Supported.

## `url` | Methods

[`domainToASCII(domain)`](https://nodejs.org/api/url.html#urldomaintoasciidomain)
: 🔴 Not implemented.

[`domainToUnicode(domain)`](https://nodejs.org/api/url.html#urldomaintounicodedomain)
: 🔴 Not implemented.

[`fileURLToPath(url[, options])`](https://nodejs.org/api/url.html#urlfileurltopathurl-options)
: 🔴 Not implemented.

[`format(URL[, options])`](https://nodejs.org/api/url.html#urlformaturl-options)
: 🔴 Not implemented.

[`pathToFileURL(path[, options])`](https://nodejs.org/api/url.html#urlpathtofileurlpath-options)
: 🔴 Not implemented.

[`urlToHttpOptions(url)`](https://nodejs.org/api/url.html#urlurltohttpoptionsurl)
: 🔴 Not implemented.

[`format(urlObject)`](https://nodejs.org/api/url.html#urlformaturlobject)
: 🔴 Not implemented. Legacy.

[`parse(urlString[, parseQueryString[, slashesDenoteHost]])`](https://nodejs.org/api/url.html#urlparseurlstring-parsequerystring-slashesdenotehost)
: 🔴 Not implemented. Deprecated.

[`resolve(from, to)`](https://nodejs.org/api/url.html#urlresolvefrom-to)
: 🔴 Not implemented. Legacy.
