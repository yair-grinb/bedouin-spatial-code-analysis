# Geospatial Analysis of Cultural Variation in Adherence to the Bedouin Spatial Code
## 1. Background
This repository contains the code implementing the analysis detailed in the paper XXX, which measures the adherence of various communities in the Mariit Valley, Israeli Negev Desert, to the Bedouin Spatial Code (BSC) - a set of cultural norms defining the ideal spatial organization of Bedouin settlements. The code reads geospatial data layers (see inputs below), processes them to compute morphological similarity measures, and then applies the EWM-TOPSIS technique to generate a unified measure of adherence to the BSC.

## 2. Requirements
The code was developed in a Python 3.12.7 environment and uses the following package dependencies:
| Package         | Version  |
|--------------- |--------- |
| GeoPandas      | 1.0.1    |
| Shapely        | 2.0.6    |
| scikit-learn   | 1.5.1    |
| NumPy          | 1.26.4    |

## 3. Inputs
To protect community privacy and due to data licensing restrictions, we cannot share the dataset. However, below are the expected input layers and their attributes:
| Input name         |  Details      | Fields     |
|------------ | -------- | ---------|
| claims      | Community boundaries layer | `claim_id` - Unique identifier for individual claims |
| bldgs      | Structures layer | `bldg_id` - Unique identifier for individual buildings |
| streams      | Water streamss layer | *No required fields* |
| basins      | Drainage basins layer | *No required fields* |
| roads      | Shigs' access roads layer | `road_id` - Unique identifier for individual roads |
| shigs      | Shigs (gathering tents/structures) layer | `shig_id` - Unique identifier for individual Shigs <br> `road_id` - Identifier of the Shig's access road (corresponds to `road_id` in the roads layer|
