Humanize.jl
===========

[![Build Status](https://travis-ci.org/IainNZ/Humanize.jl.svg)](https://travis-ci.org/IainNZ/Humanize.jl)
[![Coverage Status](https://img.shields.io/coveralls/IainNZ/Humanize.jl.svg)](https://coveralls.io/r/IainNZ/Humanize.jl)

Humanize numbers, including:

### Data sizes

`datasize(value::Number; style=:dec, format="%.1f")`

Style can be `:dec` (base 10^3), `:bin` (base 2^10), `:gnu` (base 2^10, like `ls -hs`).

```
datasize(3000000)  # "3.0 MB"
datasize(3000000, style=:bin, format="%.3f")  # "2.861 MiB"
datasize(3000000, style=:gnu, format="%.3f")  # "2.861M"
```