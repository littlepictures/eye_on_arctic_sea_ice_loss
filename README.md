# CLIP - sea ice diamond

## Background on this CLIP
The CLIP describes the decline of sea ice in the Arctic between 1980 and 2020. There are already various graphs and visualisations that impressively show the decline of the ice (in volume and also as area). The idea behind this CLIP is the radical simplification of the sea ice loss based on just two different sized shapes.

## Data Sources

The CLIP uses the following datasets:
- [ESA Sea Ice Climate Change Initiative (Sea_Ice_cci): Sea Ice Concentration Climate Data Record from the AMSR-E and AMSR-2 instruments at 25km grid spacing, version 2.1](https://data.ceda.ac.uk/neodc/esacci/sea_ice/data/sea_ice_concentration/L4/amsr/25km/v2.1/NH)
- [MET Norway](https://thredds.met.no/thredds/catalog/osisaf/met.no/reprocessed/ice/conc_450a_files/catalog.html)

## Data Preparation
The datasets were manually downloaded from the above source and processed using the open source mapping software QGIS.

To prepare the data, follow these steps:
- Load ESACCI Datasets into GIS System using EPSG:6931 WGS 84 / NSIDC EASE-Grid 2.0 North 
- Load Met.no Dataset into GIS System using EPSG:102017 WGS 84 / NSIDC EASE-Grid 2.0 North 
- Sea ice area was calculated using object properties dialogue in QGIS
- CSV was created using standard editor with columns "x","y","date", "area_m2", "color"
- x & y columns were populated with value "1" and color column was populated with lables "a" and "b" for the respective two years

## Creating Visualizations
The visualisation can be implemented using Datawrapper or similar tools. Specifically, a scatter plot was chosen that uses the identical x & y columns to position two objects on the same point. Alternatively a notebook is provided that creates an graphic in python altair to be used in vector graphics software.

To create a new datawrapper visualization, follow these steps:
- Open Datawrapper and create a new chart of the type "scatter plot".
- Load the csv file from the previous process into datawrapper
- Chose x and y columns for position, area_m2 column for size and color column for color 
- Adjust colours and transparencies and add further anotations

To create a new altair visualization, follow these steps:
- Open the python notebook provided in the scripts/dataviz folder either in your local environment or in hosted environments like Google Colab.
- Provide the path to the csv file from the previous process
- run the notebook and save the graphic from the 3-dot menue in your desired file format

## CREDITS & LICENSE
- Idea by: [UBILABS](https://ubilabs.com/)
- Processing Documentation by: [Ubilabs](https://ubilabs.com/)
- Visualization by: [UBILABS](https://ubilabs.com/)

The code in this repository is published under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/)
