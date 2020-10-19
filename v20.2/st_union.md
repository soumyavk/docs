---
title: st_union
summary: st_union is an aggregate function that combines a set of shapes into a single shape.
toc: true
---

Given a set of shapes (e.g., from a [selection query](selection-queries.html)), `st_union` combines that set of shapes into a single shape. The resulting shape can then be passed to functions that operate on a single shape, such as [`st_convexhull`](st_convexhull.html).

`st_union` works on the following data types:

- [`GEOMETRY`](spatial-glossary.html#geometry)

{{site.data.alerts.callout_info}}
The non-aggregate version of `st_union` is not implemented by CockroachDB.
{{site.data.alerts.end}}

{{site.data.alerts.callout_info}}
Unlike `st_collect`, which does not change the shapes it operates on and merely gathers them into a collection, `st_union` modifies the shapes it operates on, merging them together.
{{site.data.alerts.end}}

## Examples

XXX: WRITE ME

{% include copy-clipboard.html %}
~~~ sql
SELECT st_asgeojson(st_union(geom)) FROM bookstores WHERE geom IS NOT NULL AND address ILIKE '%, NY%';
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
- [`st_convexhull`](st_convexhull.html)
- [Migrate from Shapefiles](migrate-from-shapefiles.html)
- [Migrate from GeoJSON](migrate-from-geojson.html)
- [Migrate from GeoPackage](migrate-from-geopackage.html)
- [Migrate from OpenStreetMap](migrate-from-openstreetmap.html)
