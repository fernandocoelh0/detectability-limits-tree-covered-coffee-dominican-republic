# Data

This repository does not include the original georeferenced reference polygons used in the manuscript.

## Why the raw field polygons are not distributed

The original polygons may reveal sensitive information, including field locations, producer areas, institutional reference data or sampling locations. For this reason, the public repository should not contain raw shapefiles, GeoPackages, KML/KMZ files or other geospatial files with exact coordinates unless explicit permission for redistribution has been obtained.

## Expected input format

To run the notebooks, users should prepare their own polygon dataset with at least the following attributes:

| Field | Description |
|---|---|
| `Class` | Target class. Expected values: `coffee` and `forest`. |
| `New_ID` | Optional shade-level code for coffee polygons. Use `1` for low shade / coffee visible, `2` for intermediate shade, and `3` for high shade / forest-like coffee. |

The notebook generates a stable `sample_id` internally after reading the input file.

## Recommended public data alternatives

If data sharing is required, consider one of the following options:

1. Share an anonymised attribute table without coordinates.
2. Share a synthetic example dataset with artificial geometries.
3. Share derived sample-level predictor tables without farm names, producer identifiers or exact locations.
4. Archive restricted data in an institutional repository with controlled access.

## Files that should not be committed

Avoid committing:

- raw shapefiles or GeoPackages with exact field locations;
- producer names, farm names or private property identifiers;
- Google Earth Engine credentials or service-account keys;
- personal Google Drive paths;
- large raster files unless they are explicitly intended for public release.
