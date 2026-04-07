# SQL Query Tool for Vs30 data in Japan
SQL Query Tool for Vs30 for seismic hazard analysis in Japan (derived from J-SHIS)
***************************************

  This tool is intended for the reading and querying the SQLite 
database with a processed subset of the J-SHIS seismic hazard data (National
Research Institute for Earth Science and Disaster Resilience, NIED). It is 
specifically designed as a computational tool for high-performance spatial 
queries in seismic hazard and risk analysis and site effect modeling.

1 DATABASE
===================

  Hallo, M. (2026). Research Dataset: Optimized Site Parameters (Vs30) 
for Seismic Hazard Analysis in Japan (derived from J-SHIS) [Data set]. 
Zenodo. [https://doi.org/10.5281/zenodo.19379171](https://doi.org/10.5281/zenodo.19379171)

2 TECHNICAL IMPLEMENTATION
===================

Python 3, SQLite, SQL engine, Automatic database download, Coordinate-based indexing

*   **Zero-Configuration:** The script automatically resolves the DOI, downloads the latest SQLite database from Zenodo, and stores it locally.
*   **High-Speed SQL Queries:** Uses an optimized SQLite container with spatial indexing for rapid coordinate-based lookups.
*   **Geospatial Precision:** Performs automatic UTM projection estimation to calculate exact metric distances (km) between targets and grid points.
*   **Batch Processing:** Supports automated processing of target locations from text files.
*   **Professional Output:** Generates clean, fixed-width formatted reports with metadata and provenance tracking.

The official software version is archived on Zenodo:

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19386410.svg)](https://doi.org/10.5281/zenodo.19386410)

3 PACKAGE CONTENT
===================

  a) "jshis_sqlite_query.py" - Python script
  
  b) "example_targets.txt" - Example of input text file with target locations
  
  c) "requirements.txt" - pip requirements file for instalation of dependencies


4 REQUIREMENTS
===================

  Python: Version 3.12 or higher
  
  Libraries: pandas, geopandas, sqlalchemy, requests, shapely
  
  Install dependencies via pip:

```bash
pip install -r requirements.txt
```

5 USAGE
===================

  1. Prepare your 'example_targets.txt' file (longitude latitude pairs)
  2. Run the tool: 'python jshis_sqlite_query.py'
  3. Check 'example_results_vs30.txt' for the output Vs30

6 EXAMPLE OUTPUT
===================

This tool extracts site-specific Vs30 for a set of target Longitude-Latitude 
pairs from a SQLite database for Japan. Results are automatically saved to a 
formatted text file.
```text
# RESULTS OF VS30 FOR TARGET LOCATIONS
# Generated on: 2026-04-03 09:42:57.783795
# Target_Lon Target_Lat Lon Lat Vs30(m/s) AF(-) Dist(km)
136.9878 36.8520 136.9867 36.8515 194.5 1.8484 0.113
136.7053 34.4871 136.7047 34.4865 392.5 1.0162 0.091
136.6515 36.5661 136.6523 36.5661 338.8 1.1520 0.072
136.2588 35.2675 136.2585 35.2682 184.1 1.9374 0.082
136.2133 36.0639 136.2148 36.0640 166.8 2.1073 0.136
```

7 COPYRIGHT
===================

Copyright (C) 2026 Kyoto University

This program is published under the GNU General Public License (GNU GPL).

This program is free software: you can modify it and/or redistribute it
or any derivative version under the terms of the GNU General Public
License as published by the Free Software Foundation, either version 3
of the License, or (at your option) any later version.

This code is distributed in the hope that it will be useful, but WITHOUT
ANY WARRANTY. We would like to kindly ask you to acknowledge the authors
and don't remove their names from the code.

You should have received copy of the GNU General Public License along
with this program. If not, see <http://www.gnu.org/licenses/>.
