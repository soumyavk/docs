---
title: st_contains
summary: st_contains(A, B) returns true if no point in shape B lies outside of shape A, and at least one point in the interior of B lies in the interior of A.
toc: true
has_prefixed_variant: true
---

Given two shapes _A_ and _B_, the predicate function `st_contains(A, B)` returns `true` if:

- No point in _B_ lies outside of shape _A_, and
- At least one point in the interior of _B_ lies in the interior of _B_.

In other words, the exterior of shape _A_ must not include any point in _B_, and one or more points of _B_'s interior must lie in the interior of _A_.

This behavior is similar to [`st_covers`](st_covers.html), except that the criteria are more exacting, and therefore some pairs of shapes will be rejected by this function that would be accepted by `st_covers`.

`st_contains` works on the following data types:

- [`GEOMETRY`](spatial-glossary.html#geometry)
- [`GEOGRAPHY`](spatial-glossary.html#geography)


{% if page.has_prefixed_variant %}
{{site.data.alerts.callout_info}}
`{{page.title}}` will attempt to use any available [spatial index](spatial-indexes.html) to speed up its operation.  Use the prefixed variant `_{{page.title}}` if you do not want any spatial indexes to be used.
{{site.data.alerts.end}}
{% endif %}

{{site.data.alerts.callout_info}}
This function is the inverse of [`st_within`](st_within.html).
{{site.data.alerts.end}}

## Examples

XXX: WRITE ME

## See also

- [Working with Spatial Data](spatial-data.html)
- [Spatial and GIS Glossary of Terms](spatial-glossary.html)
- [Spatial indexes](spatial-indexes.html)
- [Spatial functions](functions-and-operators.html#spatial-functions)
- [`st_covers()`](st_covers.html)
- [`st_coveredby()`](st_coveredby.html)
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
- [Migrate from Shapefiles](migrate-from-shapefiles.html)
- [Migrate from GeoJSON](migrate-from-geojson.html)
- [Migrate from GeoPackage](migrate-from-geopackage.html)
- [Migrate from OpenStreetMap](migrate-from-openstreetmap.html)
