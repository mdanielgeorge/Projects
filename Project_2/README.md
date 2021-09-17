# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Ames Housing Data and Kaggle Challenge

## Project 2: Ames Housing Data and Kaggle Challenge

### Background

Currently working in J.S. Consultancy LLP, the team is working to provide quality advise and market research related to real estate sales.
Iowa Real Estate (IRE) has engaged our services to aid them in their expansion into Ames,Iowa.


### Problem Statement

As part of the team, our job is to assist IRE in their expansion into Ames, Iowa. With various housing estates in Ames, Iowa with different features and locations, what are the best strategies we should be looking into when purchasing houses?

Success will be evaluated by the returns for IRE after purchasing and re-sale of House

---

### Datasets

Below datasets have been used

* [`test.csv`](./data/act_2017.csv): Test data for our predictor

* [`train.csv`](./data/act_2017.csv): Train data for our machine learning

---

### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|MS SubClass|Integer|Type of dwelling| 
|MS Zoning|Object|Zone of sales| 
|Lot Frontage|float|Linear feet of street connected| 
|Lot Area|Integer|Lot size in Square Feet| 
|Street|Object|Type of road access| 
|Alley|Object|Type of alley access| 
|Lot Shape|Object|Shape of property| 
|Land Contour|Object|Flatness of property|
|Utilities|Object|Utilities available|
|Lot Config|Object|Lot Configuration|
|Land Slope|Object|Slope of property|
|Neighborhood|Object|Location with Ames City limits|
|Condition 1|Object|Proximity of various conditions|
|Condition 2|Object|Proximity of various conditions(If more than one)|
|Bldg Type|Object|Type of dwelling|
|House Style|Object|Style of dwelling|
|Overall Qual|Integer|Rates the overall material and finish of the house|
|Overall Cond|Integer|Rates the overall condition of the house|
|Year Built|Integer|Original construction date|
|Year Remod/Add|Integer|Remodel date (same as construction date if no remodeling or additions)|
|Roof Style|Object|Type of roof|
|Roof Matl|Object|Roof material|
|Exterior 1st|Object|Exterior covering on house|
|Exterior 2nd|Object|Exterior covering on house (if more than one material)|
|Mas Vnr Type|Object|Masonry veneer type|
|Mas Vnr Area|float|Masonry veneer area in square feet|
|Exter Qual|Object|Evaluates the quality of the material on the exterior|
|Exter Cond|Object|Evaluates the present condition of the material on the exterior|
|Foundation|Object|Type of foundation|
|Bsmt Qual|Object|Evaluates the height of the basement|
|Bsmt Cond|Object|Evaluates the general condition of the basement|
|Bsmt Exposure|Object|Refers to walkout or garden level walls|
|BsmtFin Type 1|Object|Rating of basement finished area|
|Bsmt SF 1|float|Type 1 finished square feet|
|BsmtFin Type 2|Object|Rating of basement finished area (if multiple types)|
|BsmtFin SF 2|float|Type 2 finished square feet|
|Bsmt Unf SF|float|Unfinished square feet of basement area|
|Total Bsmt SF|float|Total square feet of basement area|
|Heating|Object|Type of heating|
|Heating QC|Object|Heating quality and condition|
|Central Air|Object|Central air conditioning|
|Electrical|Object|Electrical system|
|1st Flr SF|Integer|First Floor square feet|
|2nd Flr SF|Integer|Second floor square feet|
|Low Qual Fin SF|Integer|Low quality finished square feet (all floors)|
|Gr Liv Area|Integer|Above grade (ground) living area square feet|
|Bsmt Full Bath|float|Basement full bathrooms|
|Bsmt Half Bath|float|Basement half bathrooms|
|Full Bath|Integer|Full bathrooms above grade|
|Half Bath|Integer|Half baths above grade|
|Bedroom AbvGr|Integer|Bedrooms above grade (does NOT include basement bedrooms)|
|Kitchen AbvGr|Integer|Kitchens above grade|
|Kitchen Qual|Object|Kitchen quality|
|TotRms AbvGrd|Integer|Total rooms above grade (does not include bathrooms)|
|Functional|Object|Home functionality (Assume typical unless deductions are warranted)|
|Fireplaces|Integer|Number of fireplaces|
|Fireplace Qu|Object|Fireplace quality|
|Garage Type|Object|Garage location|
|Garage Yr Blt|float|Year garage was built|
|Garage Finish|Object|Interior finish of the garage|
|Garage Cars|float|Size of garage in car capacity|
|Garage Area|float|Size of garage in square feet|
|Garage Qual|Object|Garage quality|
|Garage Cond|Object|Garage condition|
|Paved Drive|Object|Paved driveway|
|Wood Deck SF|Integer|Wood deck area in square feet|
|Open Porch SF|Integer|Open porch area in square feet|
|Enclosed Porch|Integer|Enclosed porch area in square feet|
|3Ssn Porch|Integer|Three season porch area in square feet|
|Screen Porch|Integer|Screen porch area in square feet|
|Pool Area|Integer|Pool area in square feet|
|Pool QC|Object|Pool quality|
|Fence|Object|Fence quality|
|Misc Feature|Object|Miscellaneous feature not covered in other categories|
|Misc Val|Integer|Value of miscellaneous feature|
|Mo Sold|Integer|Month Sold (MM)|
|Yr Sold|Integer|Year Sold (YYYY)|
|Sale Type|Object|Type of sale|
|Sale Condition|Object|Condition of sale|
|SalePrice|Integer|Sale price |
|Ttl_Bath|Integer|Total Bathrooms|
|Ttl_SF|Integer|Total Square Foot Interior|
|Ttl_ext_SF|Integer|Total Square Foot Exterior|
|sold_age|Integer|Age of house|

---

### Train Data Clean-Up

There were a total of 42 Categorical Data and 39 Numerical Data.

#### Categorical Data

Total of 15 Features with Null values found in a certain amount of rows

Below Features were dropped as it had more than 80% Null Values

* Alley
* Pool_QC
* Fence
* Misc_Feature

Fireplace_QU Null Values were filled with "Not_Applicable"

#### Numerical Data

Total of 11 Features with Null values found in a certain amount of rows

Lot_Frontage Null values were imputed with its median while the rest were dropped as they had 1% or less Null Values

---
### Exploratory Data Analysis

Looking into Features that were correlated. Below steps were taken to remove MultiCollinearity.

Combined Features

* Bathrooms were combined
* Interior Squarefoot of both basement and living area were combined
* Exterior Squarefoot of Porches and Decks were combined

Additional Feature

* Year of property sold minus Year built would equal to the Property Age

Outliers were then removed to allow a better model

---

### Modelling on Train Dataset

Two attempts of modelling was done using RidgeRegression

Atempt 1

* Train and test were scaled using StandardScaler
* Outcome of RootMeanSquared was 19312

Atempt 2

* Train and Test were not scaled
* Outcome of RootMeanSquared was 17125


Overall, Attempt 2 showed the better result.

Features influcing results 

|Feature|Coef|
|---|---|
|Overall_Qual|10472|
|Kitchen_Qual|5905|
|Neighborhood_NridgHt|5177|
|Condition_1_PosN|4838|
|Roof_Style_Hip|4075|

---

### Conclusions and Recommendations

* From the assistance of the Model, IRE should target those Features influcing SalePrice in order to achieve highest returns possible
