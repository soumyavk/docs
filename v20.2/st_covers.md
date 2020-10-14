---
title: st_covers
summary: `st_covers` returns true if no point in shape B lies outside of shape A
toc: true
---

Given two shapes _A_ and _B_, the predicate function `st_covers()` returns `true` if no point in _B_ lies outside of shape _A_.  Otherwise, it returns `false`.

In other words, shape _A_ must completely cover every point in _B_.

`st_covers` works on the following spatial data types:

- [`GEOMETRY`](spatial-glossary.html#geometry)
- [`GEOGRAPHY`](spatial-glossary.html#geography)
- [Well-known Text (WKT)](spatial-glossary.html#wkt) representations of either of the above.

{{site.data.alerts.callout_info}}
`st_covers` will attempt to use any available [spatial index](spatial-indexes.html) to speed up its operation.  Use the prefixed variant `_st_covers` if you do not want any spatial indexes to be used.
{{site.data.alerts.end}}

## Examples

## See also

+ [`st_coveredby()`](st_coveredby.html)
+ [Spatial functions and operators](functions-and-operators.html#spatial-functions)
