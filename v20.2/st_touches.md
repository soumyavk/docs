---
title: st_touches
summary: st_touches(A, B) returns true if A and B have at least one point in common, but their interiors do not intersect.
toc: true
has_prefixed_variant: true
---

Given two shapes _A_ and _B_, `st_touches(A, B)` returns `true` if:

- At least one point in the set of points that comprises _A_ is also a member of the set of points that make up _B_
- No points that make up the interior of _A_ are also part of the interior of _B_.

In other words, _A_ and _B_ have a point along their boundaries in common (i.e., they "touch"), but none of their interior points intersect.  This distinction between shapes touching along a boundary vs. intersecting is also made by the [DE-9IM](spatial-glossary.html#de-9IM) standard.

`st_touches` works on the following data types:

- [`GEOMETRY`](spatial-glossary.html#geometry)

{% if page.has_prefixed_variant %}
{{site.data.alerts.callout_info}}
`{{page.title}}` will attempt to use any available [spatial index](spatial-indexes.html) to speed up its operation.  Use the prefixed variant `_{{page.title}}` if you do not want any spatial indexes to be used.
{{site.data.alerts.end}}
{% endif %}

## Examples

XXX: WRITE ME

## See also

- [Working with Spatial Data](spatial-data.html)
- [Spatial and GIS Glossary of Terms](spatial-glossary.html)
- [Spatial indexes](spatial-indexes.html)
- [Spatial functions](functions-and-operators.html#spatial-functions)
- [`st_covers()`](st_covers.html)
- [`st_coveredby()`](st_coveredby.html)
- [`st_contains`](st_contains.html)
- [`st_within`](st_within.html)
- [`st_intersects`](st_intersects.html)
- [`st_coveredby`](st_coveredby.html)
- [`st_covers`](st_covers.html)
- [`st_disjoint`](st_disjoint.html)
- [`st_equals`](st_equals.html)
- [`st_overlaps`](st_overlaps.html)
- [`st_convexhull`](st_convexhull.html)
- [`st_union`](st_union.html)
- [Migrate from Shapefiles](migrate-from-shapefiles.html)
- [Migrate from GeoJSON](migrate-from-geojson.html)
- [Migrate from GeoPackage](migrate-from-geopackage.html)
- [Migrate from OpenStreetMap](migrate-from-openstreetmap.html)
