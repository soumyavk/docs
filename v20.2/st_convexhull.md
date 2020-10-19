---
title: st_convexhull
summary: st_convexhull(A) returns another shape B that is the convex hull of A.
toc: true
has_prefixed_variant: false
---

Given a shape _A_, `st_convexhull(A)` returns another shape _B_ that is the [convex hull](https://en.wikipedia.org/wiki/Convex_hull) of _A_.  The convex hull of a shape is the smallest [convex set](https://en.wikipedia.org/wiki/Convex_set) of points that [contains](st_contains.html) every point in the set that comprises that shape.

In other words, given a set of points _A_ in the plane, the convex hull is the shape _B_ created by stretching an imaginary rubber band around the outermost points in _A_.

`st_convexhull` works on the following data types:

- [`GEOMETRY`](spatial-glossary.html#geometry)

{{site.data.alerts.callout_info}}
`st_convexhull` is not an aggregate function.  It operates on a single `GEOMETRY` object.  This means that in practice it is most often used in combination with an aggregate function such as `st_collect`.
{{site.data.alerts.end}}

## Examples

XXX: WRITE ME

{% include copy-clipboard.html %}
~~~ sql
SELECT st_asgeojson(st_convexhull(st_union(geom))) FROM bookstores WHERE geom IS NOT NULL AND address ILIKE '%, NY%';
~~~

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
- [`st_touches`](st_touches.html)
- [`st_union`](st_union.html)
- [Migrate from Shapefiles](migrate-from-shapefiles.html)
- [Migrate from GeoJSON](migrate-from-geojson.html)
- [Migrate from GeoPackage](migrate-from-geopackage.html)
- [Migrate from OpenStreetMap](migrate-from-openstreetmap.html)
