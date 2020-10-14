---
title: st_coveredby
summary: `st_coveredby` returns true if no point in shape A lies outside of shape B
toc: true
---

Given two shapes _A_ and _B_, the predicate function `st_coveredby()` returns `true` if no point in _A_ lies outside of shape _B_.  Otherwise, it returns `false`.

In other words, shape _B_ must completely cover every point in _A_.

`st_coveredby` works on the following spatial data types:

- [`GEOMETRY`](spatial-glossary.html#geometry)
- [`GEOGRAPHY`](spatial-glossary.html#geography)
- [Well-known Text (WKT)](spatial-glossary.html#wkt) representations of either of the above.

{{site.data.alerts.callout_info}}
`st_coveredby` will attempt to use any available [spatial index](spatial-indexes.html) to speed up its operation.  Use the prefixed variant `_st_coveredby` if you do not want any spatial indexes to be used.
{{site.data.alerts.end}}

## Examples

## See also

+ [`st_covers()`](st_covers.html)
+ [Spatial functions and operators](functions-and-operators.html#spatial-functions)
