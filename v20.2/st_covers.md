---
title: st_covers
summary: st_covers returns true if no point in shape B lies outside of shape A
toc: true
---

Given two shapes _A_ and _B_, the predicate function `st_covers()` returns `true` if no point in _B_ lies outside of shape _A_.  Otherwise, it returns `false`.

In other words, shape _A_ must completely cover every point in _B_.

`st_covers` works on the following spatial data types:

- [`GEOMETRY`](spatial-glossary.html#geometry)
- [`GEOGRAPHY`](spatial-glossary.html#geography)
- [Well-known Text (WKT)](spatial-glossary.html#wkt) representations of either of the above.

{{site.data.alerts.callout_info}}
`{{page.title}}` will attempt to use any available [spatial index](spatial-indexes.html) to speed up its operation.  Use the prefixed variant `_{{page.title}}` if you do not want any spatial indexes to be used.
{{site.data.alerts.end}}

## Examples

XXX: WRITE THIS

## See also

+ [`st_coveredby()`](st_coveredby.html)
+ [Spatial functions and operators](functions-and-operators.html#spatial-functions)

- [`st_contains`](st_contains.html)
- [`st_within`](st_within.html)
- [`st_intersects`](st_intersects.html)
- [`st_coveredby`](st_coveredby.html)
- [`st_covers`](st_covers.html)
- [`st_disjoint`](st_disjoint.html)
- [`st_equals`](st_equals.html)
- [`st_overlaps`](st_overlaps.html)
- [`st_touches`](st_touches.html)
- [`st_convexhull`](st_convexhull.html)
- [`st_union`](st_union.html)
