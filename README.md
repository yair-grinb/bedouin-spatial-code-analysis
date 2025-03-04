# Geospatial Analysis of Cultural Variation in Adherence to the Bedouin Spatial Code
## 1. Background
This repository includes the code implementing the analysis detailed in the paper XXX, meant to measure the adherence of various communities in the Mariit Valley in the Israeli Negev Desert to the Bedouin Spatial Code (BSC) - a set of cultural normal defining an ideal form for Bedouin settlments. The code reads geodata layers (see inputs below), processes them to compute morphological similarity measures, and then uses the EWM-TOPSIS technique to produce a unified measure of adhernece to the BSC. 

## 2. Requirements
The code was developed in a Python 3.12.7 environment and uses the following packages and versions:
| Package         | Version  |
|--------------- |--------- |
| GeoPandas      | 1.0.1    |
| Shapely        | 2.0.6    |
| scikit-learn   | 1.5.1    |
| NumPy          | 1.26.4    |

## 3. Inputs
To protect the privacy of communities in the area and due to issues of data licenses, we cannot share the data along with the code here. However, here are details about the expected inputs:
| Input name         |  Details      | Fields     |
|------------ | -------- | ---------|
| claims      | Community boundaries layer | *claim_id* - identifier for individual claims |
| bldgs      | Structures layer | *bldg_id* - identifier for individual buildings |
| streams      | Water streamss layer |  |
| basins      | Drainage basins layer |  |
| roads      | Shigs' access roads layer | *road_id* - identifier for individual roads |
| shigs      | Shigs (gathering tents/structures) layer | *shig_id* - identifier for individual claims <br> *road_id* - identifier of the access road for the Shig, corresponds to the *road_id* field in the roads layer|
