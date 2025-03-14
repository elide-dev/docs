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
```Python
# python can of course import python
from my_app import x, y, z
```
```JavaScript
// from typescript, javascript
import { x, y, z } from "./my-app.py"

// cjs and esm are supported
const { x, y, z } = require("./my-app.py")
```

## Language Engine

%product% can execute Python using [GraalPython](https://github.com/oracle/graalpython) from Oracle.

| -------- | ---------------------------------------------------- |
| Language | **Python**                                           |
| Standard | `3.11.x`                                             |
| Maturity | ![Alpha](https://img.shields.io/badge/-alpha-blue)   |
| Engine   | [GraalPython](https://github.com/oracle/graalpython) |
