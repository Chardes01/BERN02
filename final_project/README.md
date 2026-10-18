# Urban Heat Map Prediction Modelling

## 1. Project Overview

This project investigates the use of a statistical model (Lasso + Ridge) and a convolutional neural network (CNN) to predict urban heat maps for Malmö. Municipal open data from [Malmö Open Data](https://opendata.malmo.se/) and climate data from ECMWF are used to predict the Universal Thermal Climate Index (UTCI), modelled using SOLWEIG.

## Lasso + Ridge Model


## 2. CNN-Model

A CNN is trained on spatially gridded input data to predict UTCI values. CNNs can learn spatial patterns and relationships between neighbouring grid cells, making them suitable for spatial prediction tasks. SOLWEIG-generated UTCI maps serve as target data for supervised training.

## 3. Data Sources and Licences

### Malmö Open Data

Source: [opendata.malmo.se](https://opendata.malmo.se/)
According to the data portal, its open data may be freely used, modified, and shared by private individuals and private and public organizations. For some datasets explicit Licenses are given.

Municipal datasets are used to represent relevant urban characteristics.
- [Heat maps](https://opendata.malmo.se/en/@malmo/varmekarteringar) (Creative Commons CCZero): entails the UTCI modelled based on a [SOLWEIG model](https://umep-docs.readthedocs.io/en/latest/OtherManuals/SOLWEIG.html) 
- [The primary map](https://opendata.malmo.se/en/%40malmo/primarkartan) (cc0-1.0): here utilized: Buildings.geojson.
- [Tree canopy](https://opendata.malmo.se/en/%40malmo/tradkrontackning-2022)(no License given): proportion of the city covered by greenery.
- [Landsurface](https://opendata.malmo.se/en/@malmo/varmekarteringar) (no License given): The following layers were used: Residential areas, Paved and artificial surfaces, Industrial areas, Cemeteries, Natural areas, Parks and green spaces, Open land, Special recreational areas, Plot and property land, Water bodies

### ECMWF Climate Data

[ERA5-Land hourly data from 1950 to present](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-land?tab=overview)(CC-BY licence): 2m temperature

Cimate scenario modifications were based on [SMHI](https://www.smhi.se/en/climate/tools-and-inspiration/climate-change-scenario/climate-change-scenario-tool/met/skane_lan/medeltemperatur/rcp85/2041-2070/summer/anom) climate scenario tool for RCP4.5 and RCP8.5.


## 4. Folder Structure


```text
final_project/
├── README.md
├── LICENSE
├── requirements.txt
├── data/
│   ├── processed_5m/       # prepared data for a resolution of 5m
│       └── input/         # static input files (buildings, tree canopy, landuse)
│       └── targets/         # SOLWEIG-generated UTCI maps
│       └── climate/         # 2m temperature data and modified for climate scenarios
├── notebooks/           # Exploration and experiments
├── src/
│   ├── preprocessing/   # Data preparation
│   ├── models/          # CNN architecture
│   ├── training/        # Training and validation
│   └── evaluation/      # Metrics and visualisations
├── outputs/
│   ├── predictions/     # Predicted UTCI maps
│   ├── figures/         # Plots and evaluation results
│   └── checkpoints/     # Saved model weights
└── tests/               # Tests, if applicable
```

## 5. Reproducibility

For reproducibility, document dataset versions, preprocessing steps, model configuration, training settings, data splits and evaluation metrics. Large datasets, temporary files and model checkpoints should generally be excluded from Git unless necessary, using a `.gitignore` file.

### License

The Code is distributed under the MIT License. See LICENSE.txt for more information. The original data is distributed under the named licenses.
