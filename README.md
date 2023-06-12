
# Clustering a 5GDHC network
## MSc Thesis Engineering and Policy Analysis
### Sarah van Burk

This project provides a tool to divide a certain urban area into several clusters, which can be used in the design stage of a 5GDHC network. This model is part of an MSc thesis. The methodologies used in this project are elaborately discussed in this thesis. The thesis is stored in this folder as well as MScEPA_Thesis_Sarah_van_Burk_4548906_Final.pdf

In this project data of a case study on the inner city of Amsterdam is provided. Other cases can be implemented in the model as well, but may require a whole different data preparation

Four Python files are included at the root of this folder. The input data for the model files are stored in the data folder. The file Data_preperation.ipynb, stored in the root of this folder, creates the dataframes used in the model, and also stores them in the data folder. Several variables are used to create the input data for the model. These variables are important since they are necessary to run the model. The following variables with the building date are needed:

1. geometry: the location of the building
2. x: the x coordinate (split of the geometry)
3. y: the y coordinate (split of the geometry)
4. point: a combination of the x and y coordinate in string format
5. oppervlakt: the surface of the building in m^2
6. Hoofdfun_1: the function of the building described in a letter (only for non-residential buildings)
7. Q_c_kWh: the potential waste heat in kwh (only for non-residential buildings)
8. openbare_r: the street in which the building is located (not necessary when using ZIP-codes)
9. postcode: the ZIP-code in which the building is located
10. coldest_day: the aggregated demand or supply over the coldest day in kwh
11. coldest_month: the aggregated demand or supply over the coldest month in kwh
12. whole_year: the aggregated demand or supply over the whole year in kwh

This Python project exists of 3 separate model files. The Clustering_model.ipynb can be seen as the main file. This file takes the dataframes created in the data preparation and creates the clusters. Attention needs to be paid to the parameter settings at the beginning of the file.

The other two Python files in the root of this folder are provided to calculate the performance metrics identified in the thesis. The Routing.ipynb provides a tool to calculate the total length of all clusters identified in the clustering model. The Energy_balance.ipynb file calculates the disbalance or the lack of supply of the identified clusters.

The results of all model files are stored in the folder results. An Excel file with a short data analysis on the performance metrics is also stored in this folder. Additionaly, the high quality figures of the results are stored in this folder.
