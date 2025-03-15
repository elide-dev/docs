# WinterTC

[WinterTC](https://wintertc.org/) (AKA ECMA International Technical Committee 55) is an and open collaborative group
committed to standardizing web-facing JavaScript runtimes; "web-interoperable" describes a package of new standards and
definitions:

- **[Minimum Common API][0]**: Defines a standard set of "minimum common APIs" which all web-interoperable runtimes
  should support.

- **[Sockets API](https://sockets-api.proposal.wintertc.org/)**: Defines APIs for communicating over custom TCP sockets
  from non-browser JavaScript applications.

- **[CLI API](https://github.com/wintercg/proposal-cli-api)**: Defines standards for accessing system environment,
  invocation arguments, and other CLI-related APIs.


## Elide + WinterTC

Elide aims to conform to most WITC standards:

| Standard               | Links                | Standards Body  | Description                                  | Status       |
|------------------------|----------------------|-----------------|----------------------------------------------|--------------|
| **Minimum Common API** | [Spec][0], [Repo][1] | WinterTC (TC55) | Minimum APIs for web-interoperable runtimes  | ✅ Conforms   |
| CLI API                | [Repo][2]            | WinterTC (TC55) | Uniform CLI-related APIs for non-browsers    | ✨ On the way |
| Sockets API            | [Spec][3], [Repo][4] | WinterTC (TC55) | Custom TCP sockets from non-browser contexts | ✨ Someday    |
| Fetch API              | [Spec][5], [Repo][6] | WHATWG          | Standard WhatWG Fetch API, from non-browsers | ✅ Conforms   |
| Web Crypto Streams     |                      | WHATWG          | Streaming options for Web Crypto APIs        | ✨ Someday    |

[0]: https://min-common-api.proposal.wintertc.org/
[1]: https://github.com/wintercg/proposal-minimum-common-api
[2]: https://github.com/wintercg/proposal-cli-api
[3]: https://sockets-api.proposal.wintertc.org/
[4]: https://github.com/wintercg/proposal-sockets-api
[5]: https://fetch.spec.whatwg.org/
[6]: https://github.com/whatwg/fetch
