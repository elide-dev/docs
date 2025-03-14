# Ruby

%product% can execute your Ruby applications, while integrating with other languages like JavaScript and Python.

> Elide ships with Ruby disabled by default. This restriction will be lifted in a future release.
{style="warning"}

```Console
elide run --ruby ...
```
```Ruby
def hello
  puts "Elide can run Ruby!"
end
```

## Language Engine

%product% executes Ruby using [TruffleRuby](https://github.com/oracle/truffleruby) from Oracle.

| -------- | ---------------------------------------------------- |
| Language | **Ruby**                                             |
| Standard | [MRI](https://en.wikipedia.org/wiki/Ruby_MRI) `3.2`  |
| Maturity | ![Alpha](https://img.shields.io/badge/-alpha-blue)   |
| Engine   | [TruffleRuby](https://github.com/oracle/truffleruby) |
