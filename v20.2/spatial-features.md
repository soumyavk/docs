---
title: Spatial Features
summary: A summary of CockroachDB's support for storing and querying spatial data.
toc: true
---

<span class="version-tag">New in v20.2</span>: CockroachDB supports efficiently storing and querying spatial data.

{{site.data.alerts.callout_info}}
This documentation is still being worked on for the 20.2 release. For now, see the getting started tutorial in [Working with Spatial Data](spatial-data.html).
{{site.data.alerts.end}}

## Spatial functions

In addition to the [generated reference documentation for spatial functions](functions-and-operators.html#spatial-functions), we have written additional documentation for the following functions, including examples:

- [`st_contains`](st_contains.html)
- [`st_convexhull`](st_convexhull.html)
- [`st_coveredby`](st_coveredby.html)
- [`st_covers`](st_covers.html)
- [`st_disjoint`](st_disjoint.html)
- [`st_equals`](st_equals.html)
- [`st_intersects`](st_intersects.html)
- [`st_overlaps`](st_overlaps.html)
- [`st_touches`](st_touches.html)
- [`st_union`](st_union.html)
- [`st_within`](st_within.html)

## See also

- [Working with Spatial Data](spatial-data.html)
- [Spatial and GIS Glossary of Terms](spatial-glossary.html)
- [Spatial functions](functions-and-operators.html#spatial-functions)
- [Migrate from Shapefiles](migrate-from-shapefiles.html)
- [Migrate from GeoJSON](migrate-from-geojson.html)
- [Migrate from GeoPackage](migrate-from-geopackage.html)
- [Migrate from OpenStreetMap](migrate-from-openstreetmap.html)
