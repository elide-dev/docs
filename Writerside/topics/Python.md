# Python

%product% can run Python applications under the Python 3 language standard; %product% behaves nearly identically to
CPython.

```Console
elide ./script.py
```
```Python
def hello():
  print("Elide can run Python!")
```

## Language Engine

%product% can execute Python using [GraalPython](https://github.com/oracle/graalpython) from Oracle.

| -------- | ---------------------------------------------------- |
| Language | **Python**                                           |
| Standard | `3.11.x`                                             |
| Maturity | ![Alpha](https://img.shields.io/badge/-alpha-blue)   |
| Engine   | [GraalPython](https://github.com/oracle/graalpython) |
| Tools    | [uv](https://astral.sh) (see [Python Tooling](Python-Tooling.md)) |

## Python Interop

Developers can expose Python symbols (functions, classes, and values) to the [polyglot context](101-Polyglot-Context.md)
using the `elide` built-in module:

<code-block lang="Python">
from elide import bind, poly

@bind
def say_hello(name = "Python"):
  """Render a hello greeting to the specified name."""
  return f"Hello, {name}!"

# use `poly` if you want to rename the symbol
# (it's shorthand for 'polyglot')
@poly(name = "goodbye")
def say_goodbye(name = "Python"):
  """Render a goodbye greeting to the specified name."""
  return f"Goodbye, {name}!"

# you can return other functions and complex types!
@bind
def message(leaving = False):
  """Return a message renderer based on the user's disposition."""
  if leaving:
    return say_goodbye
  return say_hello
</code-block>

**Now, from TypeScript, for example:**

<code-block lang="TypeScript">
import { message } from "./my-python.py"

console.log(JSON.stringify({hello: message()()}))
console.log(JSON.stringify({goodbye: message(true)()}))
</code-block>

<code-block lang="Console" prompt=">">
elide ./my-index.ts
</code-block>

<code-block lang="Console">
{"hello": "Hello, Python!"}
{"goodbye": "Goodbye, Python!"}
</code-block>
