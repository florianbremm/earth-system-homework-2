# ECMWF AIFS Data Download and Visualization

Practical example for downloading and visualizing ECMWF AIFS (Artificial Intelligence/Integrated Forecasting System) surface forecast data using ECMWF Open Data.

This repository contains material developed as part of the homework assignment for the *Earth System Data Processing* course at the University of Cologne (Winter Semester 2025/26).

## Content

- **`data_access/AIF.ipynb`**: Jupyter notebook demonstrating how to download AIFS Single (deterministic) surface forecasts from ECMWF Open Data and create global visualizations
- **`environment.yml`**: Conda environment with all required dependencies
- **`data_access/aifs_input_output_fields.png`**: AIFS architecture diagram showing model input/output fields

## Quick Start

### 1. Create and activate the Conda environment

```bash
conda env create -f environment.yml
conda activate aifs
```

### 2. Run the Notebook

Open `data_access/AIF.ipynb` in Jupyter Lab or VS Code and execute the cells sequentially.

## Requirements

All dependencies are specified in `environment.yml`:
- Python 3.11
- earthkit-data (ECMWF Open Data client)
- xarray + cfgrib (GRIB2 file reading)
- matplotlib + cartopy (visualization)
- eccodes (GRIB decoding library)

## Data Volume Estimates

**Per GRIB2 file** (4 variables, one forecast step):
### 2. Run the notebook

```bash
jupyter lab data_access/AIF.ipynb
```

Or open in VS Code with the Jupyter extension.

## What the Notebook Does

- Downloads 3 recent days of AIFS Single surface forecasts (12 UTC initialization)
- Variables: 2m temperature, 10m winds, mean sea level pressure
- Forecast steps: +6h, +12h, +24h
- Saves data as GRIB2 files (~22 MB total)
---

**Course**: Earth System Data Processing, University of Cologne, Winter Semester 2025/26  
**Instructor**: Martin Schultz, Jülich Supercomputing Centre & University of Cologne  
**Assignment**: Homework on accessing and processing ECMWF AIFS data  
**Author**: Yeganeh Khabbazian
**Tools**: Developed with assistance from GitHub Copilot