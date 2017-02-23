## Fraud-Detection-of-NY-Property-Data
##### Applying fraud analysis in the NY Property Tax dataset with 1048575 observations and 30 variables
====

##### File name: NY_property_data Source 
##### Url: https://data.cityofnewyork.us/Housing-Development/Property-Valuation-and-Assessment-Data/rgy2-tti8
##### Data Provided by: Department of Finance (DOF)
##### Dataset Owner: NYC OpenData 
##### Category: Housing & Development

##### Date Created: September 2, 2011 Metadata Last Updated: September 5, 2014
##### Data volume: 1048575 Fields: 30 fields, 16 continuous, 12 categorical, 2 text 
##### Details variables: RECORD, BBLE, BLOCK, LOT, EASEMENT, OWNER, BLDGCL, TAXCLASS, LTFRONT, LTDEPTH, STORIES, FULLVAL, AVLAND, AVTOT, EXLAND, EXTOT, EXCD1, STADDR, ZIP, EXMPTCL, BLDFRONT, BLDDEPTH, AVLAND2, EXLAND2, EXLAND2, EXTOT2, EXCD2, PERIOD, YEAR, VALTYPE.
##
## Purpose of the project
* Build metrics and detect the potential fraud records
##

## Outline of Approach
##### Step1: Data Cleaning
* Data Quality Report (DQR)
* Create 50 more insightful variables based on original variables
* Partition based on 7 key metrics
* Dealing with missing value, Z-scale

##### Step2: PCA (Principle Componenet Analysis)
* PCA (Visualization, Decide to use 13 PCs)

##### Step3: Set Fraud Score: 
###### 1. Euclidean Distance
* Based on projection of original features on the 13 PCs' directions
* Calculate the euclidean distance to the origin as the fraud score

###### 2. Auto-encoder(Neural Network Algorithm)
* Use h2o package to implement auto-encoder
* Output results from the PCA serves as the input
* Set two hidden layers, both five features 
* Calculate MSE of each record as the fraud score

###### 3. Comparison
* 76% overlapping in the highest 10000 fraud scores between Euclidean Distance and Auto-encoder           

###### 4. Discover insights
* Check the 30 records with top fraud scores and identify fraud patterns within them.

====
Keep updating...
