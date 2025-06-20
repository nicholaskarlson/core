# Arkansas Counties Example Data Directory

This directory contains data files generated by the Arkansas Counties QGIS example.

## Generated Files

When you run `arkansas_counties_example.py`, the following files will be created:

### Downloaded Data
- `tl_2023_us_county.zip` (80MB) - US counties shapefile archive from Census Bureau
- `tl_2023_us_county.shp` (126MB) - US counties shapefile (main geometry file)
- `tl_2023_us_county.dbf` (971KB) - Attribute data for counties
- `tl_2023_us_county.shx` (26KB) - Spatial index file
- `tl_2023_us_county.prj` (165B) - Projection information
- `tl_2023_us_county.cpg` (5B) - Code page file
- `tl_2023_us_county.shp.*.xml` - Metadata files

### Processed Data
- `arkansas_counties.gpkg` (4.5MB) - Arkansas counties only (GeoPackage format)

### Visualizations
- `arkansas_counties_analysis.png` (926KB) - 4-panel analysis plot
- `arkansas_counties_interactive.html` (6.8MB) - Interactive web map

## Note on Version Control

These data files are **excluded from Git** via `.gitignore` because:
- They are large (total ~220MB)
- They can be regenerated by running the example script
- GitHub has file size limits (100MB per file)

## Regenerating Data

To recreate all data files, simply run:

```bash
python arkansas_counties_example.py
```

The script will:
1. Download fresh data from the US Census Bureau
2. Process and filter for Arkansas counties
3. Generate all visualizations
4. Prepare data for QGIS integration

## Data Sources

- **US Counties**: US Census Bureau TIGER/Line Shapefiles 2023
- **URL**: https://www2.census.gov/geo/tiger/TIGER2023/COUNTY/
- **License**: Public domain (US government data)
- **Update Frequency**: Annual
