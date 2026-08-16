# Raw Data

This directory contains raw input files used for preprocessing.

All raw data were downloaded using **Google Earth Engine**.  
The corresponding GEE scripts are available in `../0_gee_downloads.ipynb`.

## Data sources

| Dataset | Variables | GEE Asset / Product |
|---------|-----------|---------------------|
| ERA5-Land daily aggregates | temperature, precipitation, snow cover, albedo, radiation, wind, soil moisture | `ECMWF/ERA5_LAND/DAILY_AGGR` |
| MODIS MOD10A1 | snow cover, snow albedo | `MODIS/061/MOD10A1` |
| MODIS MOD11A1 | land surface temperature | `MODIS/061/MOD11A1` |
| SRTM GL1 | elevation, slope, aspect | `USGS/SRTMGL1_003` |
| Shemonaikha station SWE | observed SWE | local CSV (`shemonaikha.csv`) |

## How to reproduce

1. Open `../0_gee_downloads.ipynb` in Google Earth Engine.
2. Run the scripts for each dataset and export the CSVs.
3. Place the downloaded files in this directory.
4. Run `../1_data_preprocessing.ipynb` to create the final processed dataset.

> Note: Raw data files are not committed to this repository to avoid redistribution restrictions and large file sizes.
