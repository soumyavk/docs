---
title: st_coveredby
summary: st_coveredby returns true if no point in shape A lies outside of shape B
toc: true
has_prefixed_variant: true
---

Given two shapes _A_ and _B_, the predicate function `st_coveredby()` returns `true` if no point in _A_ lies outside of shape _B_.  Otherwise, it returns `false`.

In other words, shape _B_ must completely cover every point in _A_.

`st_coveredby` works on the following spatial data types:

- [`GEOMETRY`](spatial-glossary.html#geometry)
- [`GEOGRAPHY`](spatial-glossary.html#geography)


{% if page.has_prefixed_variant %}
{{site.data.alerts.callout_info}}
`{{page.title}}` will attempt to use any available [spatial index](spatial-indexes.html) to speed up its operation.  Use the prefixed variant `_{{page.title}}` if you do not want any spatial indexes to be used.
{{site.data.alerts.end}}
{% endif %}

## Examples

XXX: WRITE THIS

## See also

+ [`st_covers()`](st_covers.html)
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
- [Working with Spatial Data](spatial-data.html)
- [Spatial and GIS Glossary of Terms](spatial-glossary.html)
- [Spatial functions](functions-and-operators.html#spatial-functions)
- [Migrate from Shapefiles](migrate-from-shapefiles.html)
- [Migrate from GeoJSON](migrate-from-geojson.html)
- [Migrate from GeoPackage](migrate-from-geopackage.html)
- [Migrate from OpenStreetMap](migrate-from-openstreetmap.html)
