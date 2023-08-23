# little picture - arctic sea ice loss

## Background on this little picture
_a decline? Arctic sea ice in 1980 compared to 2016_

Satellite observations have been instrumental in monitoring Arctic sea ice extent and thickness, and its changes over time.
From space sensors, can track seasonal and long-term trends. Arctic ice cover is shown to shrinking at an alarming rate, leading to concerns about its impact on the regional and global climate system. By continuously monitoring Arctic sea ice from space, researchers can better understand the dynamics of this critical component of our planet&#39;s climate system and make informed decisions to address the challenges posed by its decline. This data-driven graphic represents the area of arctic sea ice observed by satellites in 1980 compared to 2016.

https://climate.esa.int/en/little-pictures-gallery/An-eye-on-sea-ice-loss/

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
