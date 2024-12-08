# Houston Blackout Analysis: Texas Winter Storm

## Author
- **Takeen Shamloo**  
  GitHub: [@takeenshamloo](https://github.com/takeenshamloo)

## Overview
This repository explores the geospatial and socioeconomic impacts of the 2
021 Texas Winter Storm on power outages in the Houston metropolitan area. 
By analyzing remotely sensed night light data, roads, housing, and census 
information, we identify areas that experienced blackouts and assess their 
correlation with socioeconomic factors.

### Repository Purpose
This repository showcases skills in:
- Raster and vector data manipulation.
- Spatial joins and CRS transformations.
- Geospatial analysis with socioeconomic data integration.
- Professional data visualization and interpretation.

---

## Contents

The repository is structured as follows:
```{plaintext}
Houston_Blackout_Analysis
├── output/
│   ├── houston_storm_analysis.html     # HTML render of document
│   ├── houston_storm_analysis_files/  # Output figures etc.
├── docs/
│   ├── houston_storm_analysis.qmd     # Quarto analysis document
├── README.md                             
├── .gitignore                         # Files and folders excluded from Git tracking
```

**Important:**  
The `data/` folder contains raw input files and is excluded from the repository using `.gitignore`.

---

## Data Sources
1. **Night Lights Data**
   - **Source**: NASA’s VIIRS dataset from the Suomi NPP satellite.
   - **Files**: Pre-storm (2021-02-07) and post-storm (2021-02-16) raster tiles.

2. **Roads and Housing Data**
   - **Source**: OpenStreetMap via Geofabrik.
   - **Files**: Geopackages for roads and housing in the Houston metropolitan area.

3. **Socioeconomic Data**
   - **Source**: U.S. Census Bureau's 2019 American Community Survey.
   - **Files**: Geodatabase of census tract geometries and income data.

---

## Key Analyses and Outputs
1. **Blackout Detection**
   - Created a mask of areas experiencing a significant drop in night light intensity (>200 nW cm⁻² sr⁻¹).
   - Excluded highways and buffered regions (200m) to minimize false positives.

2. **Housing Impact**
   - Identified residential buildings within blackout-affected areas.
   - Estimated the number of homes impacted: **28,663 homes**.

3. **Socioeconomic Correlation**
   - Linked blackout data to census tracts.
   - Generated plots comparing income distributions for tracts with and without blackouts.

4. **Visualizations**
   - Pre- and post-storm night light intensity maps.
   - Houston blackout map with affected homes.
   - Income distribution boxplot by blackout status.

---

## Skills Demonstrated
- **Geospatial Analysis**
  - Vectorization, spatial cropping, and buffer operations.
  - Raster analysis using difference calculations and masking.

- **Data Visualization**
  - Maps and plots with clear legends, titles, and appropriate color scales.

- **Reproducibility**
  - Organized workflow and detailed comments for interpret ability.
  - Quarto documents rendered to HTML.

---

## Acknowledgements
- This project was developed as part of the UCSB MEDS program.
- Data sources include NASA’s VIIRS, OpenStreetMap, and U.S. Census Bureau.

## Reflections
This analysis reveals disproportionate impacts of the storm on lower-income neighborhoods in Houston. Limitations include the use of census-level data. Future improvements could involve higher-resolution datasets and additional socioeconomic indicators.
