# CLIP# sea ice diamond<img style="float: right;" src="https://raw.githubusercontent.com/trevalabs/.github/main/logos/trevelabs_logo.png" width="180">
<hr>

## TrevaLabs
 
[TrevaLabs](https://www.TrevaLabs.com) is a collective of climate data visualisation creatives in Europe, brought together by the desire to make a big impact with little pictures. Its mission is to rapidly create little pictures of climate for maximal human impact, and the vision is to reach every European by the end of decade with a little picture on Climate.

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
The visualisation was implemented using Datawrapper. Specifically, a scatter plot was chosen that uses the identical x & y columns to position two objects on the same point.  

To create a new visualization, follow these steps:
- Open Datawrapper and create a new chart of the type "scatter plot".
- Load the csv file from the previous process into datawrapper
- Chose x and y columns for position, area_m2 column for size and color column for color 
- Adjust colours and transparencies and add further anotations

## CREDITS & LICENSE
- Idea by: [UBILABS](https://ubilabs.com/)
- Processing Documentation by: [Ubilabs](https://ubilabs.com/)
- Visualization by: [UBILABS](https://ubilabs.com/)

The code in this repository is published under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/)
