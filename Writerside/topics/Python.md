# Python

%product% can run Python applications under the Python 3 language standard; %product% behaves nearly identically to
CPython.

```Console
elide run --python ...
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
