# Modelling Health Conditions in Cote d'Ivoire and Senegal using Call Detail Records (CDR)

## Requirements
* Python
  * Pandas
  * Numpy
  * Matplotlib
  * Statsmodel
  * Dask
* R
  * data.table
  * fBasics
  * lmtest
  * mctest

## Get the Data

* ### CDR Data

 The CDR Data for Cote d'Ivoire can be downloaded from the following links respectively:
 
 * [Cote d'Ivoire](http://yahoo.co.uk)
 * [Senegal](http://yahoo.co.uk)

The Cote d'Ivoire CDR directory must be named SET1TSV and contain files with the extension .TSV. The SET1TSV directory must be placed in the CDR_Data_IC directory provided in the respository. The Senegal CDR directory must be named SET1 and contain files with the extension .CSV. The SET1 directory must be placed in the CDR_Data_Sen directory provided in the repository.

* ### DHS Feature Extraction

To extract the information pertaining the four health indicators, the following python notebooks should be run:
* **HIV rate** - AR_Notebook
* **Child Mortality Rate** - ChildMortality_Notebook
* **Malaria Rate** -  Household_Notebook
* **Women's Access to Health** - Womens_Health_Acc_Notebook

Each python will generate .csv files per administrative level (1 - 3) in Cote d'Ivoire and Senegal containing the relative distribution of the health indicators in each region. The results for Cote d'Ivoire and Senegal can be found in the IC_DHS and SEN_DHS directories respectively. Both directories are arranged with the following sub-directories:

  * **ciar61sv** - contains aids recode file and generated csv files pertaining regional distribution of HIV at all administrative levels.
  * **cibr62sv/snbr6dsv**- contains birth recode file and generated csv files pertaining regional distribution of child mortality at all administrative levels.
  * **cihr62sv/snhr6dsv** - contains household recode file and generated csv files pertaining regional distribution of malaria at all administrative levels.
  * **ciir62sv/snir6dsv** - contains individual recode file and generated csv files pertaining regional distribution of women's access to ealth at all administrative levels.
  * **Cluster_to_Region** - contains csv file mapping of DHS cluster to region in administrative levels 1 to 3.
  * **Region_Population** - contain csv file detailing population contained in each DHS cluster voronoi polygon.
  * **Voronoi_clusters/Proportions** - contains csv files detailing the proportion of DHS cluster voronoi polygon overlapping with each region at all administrative levels.
  
    * ### CDR Feature Extraction
  
  To extract information pertaining the CDR metrics for both Cote d'Ivoire and Senegal, the *CDR_Analysis* python notebook should be run. Take note that due to the large size of the CDR datasets, the script will take on average 30mins to generate the required .csv files for both countries. The results for both countries will be found in the CDR_Data_IC and CDR_Data_Sen for Cote d'Ivoire and Senegal respectively. These directories are organized as follows:
  
  * **Activity/Introversion/Gravity_Residual/Network_Advantage** - These are sub-directories that will contain the generated csv files concerning the regional distribution of the metrics at all administrative levels.
  * **region_centroids** - contains csv files detailing geo-locations of the centroids of each region at all administrative levels.
  * **Region_Population** - contains csv files detailing the population contained in each region at all administrative levels.
  * **Voronoi_Polygons/Proportions** - contains csv files detailing the proportion of the cell antenna voronoi polygons overlapping with each region at all administrative levels.
  * **Points_In_Polygons** - contains csv files detailing the total number of cell antennas in each region per administrative level.
  * **ANT_POS.TSV/SITE_LONLAT.CSV** - details the geo-locations of cell antennas in Cote d'Ivoire/Senegal.
  
  
  
