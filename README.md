# data5100-climate-agriculture
Project repository for DATA 5100 (Foundations of Data Science) for the MS Data Science program at Seattle University.

Fall 2022 | Alexander Churchill, Malia Cortez, McKenzie Maidl, Yootaek Oh

## Problem Statement
**How has and how will climate change impact apple yields in Washington state?**

To answer this, we broke the question down into the following smaller questions:

- How have different climatic variables changed over time?
- Is there evidence of changes in apple production in the state?
    - Have annual apple yields changed, and has the yield per tree changed?
- How do different climatic factors impact the yields?
- How do we forecast apple yields per tree to change over the next 5 years?

## Repository Contents

### Data

#### Raw Data
Contains data files on climate and apples before they were cleaned.

##### Apple Data
The following dataset is from the United States Department of Agriculture Census of Agriculture for Washington state (multiple years, collected from PDF formats of census reports):
- apple_production_farms: apple trees and farm counts by year for Washington state

The following datasets are each from the United States Department of Agriculture National Agricultural Statistics Service: 
- USDA_NASS_WA-apples_1889-2010: apple production data for Washington state, 1889 - 2010
- WA_apple_production_2007_2022: apple production data for Washington state, 2007 - 2022
- WA_apple_yields_lb_acre_2007-2021: apple yields data for Washington state, 2007 - 2021
- WA_apples_bearing_2007_2021: apple bearing acres data for Washington state, 2007 - 2021
- WA_apple_price_1909_2021: apple price data for Washington state, 2007 - 2021
- WA_apples_utilized_production_2007_2021: apple utilized production data for Washington state, 2007 - 2021

##### Climate Data
The following datasets are county-level data from the Parameter-elevation Regressions on Independent Slopes Model (PRISM) Climate Group, at the Northwest Alliance for Computational Science and Engineering:
- **Adams**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Adams County, 1895 - 2021
- **Benton**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Benton County, 1895 - 2021
- **Chelan**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Chelan County, 1895 - 2021
- **Douglas**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Douglas County, 1895 - 2021
- **Franklin**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Franklin County, 1895 - 2021
- **Grant**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Grant County, 1895 - 2021
- **Klickitat**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Klickitat County, 1895 - 2021
- **Okanogan**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Okanogan County, 1895 - 2021
- **WallaWalla**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Walla Walla County, 1895 - 2021
- **Yakima**: Monthly weather data (precipitation, min/max/mean temperature, temperature differences, and min/max vapor pressure deficits) for Yakima County, 1895 - 2021


#### Cleaned Data
Contains cleaned and merged versions of the raw data files.

- WA_apples_1889_2021: merged apple data from 1889 - 2021
- apples_1970: subset of needed columns, 1970 - 2021
- apples_years: a merged apple/climate dataset used in modeling
- prism.csv: a complete version of the raw PRISM data with every county of study with separated year/month columns, 1895-2021

#### GIS Data
Contains water and county shape data for Washington state.

### Colab Notebooks
These notebooks contain the code that was used for this project.

#### Data Cleaning
- AppleData_Cleaning: loaded raw apple data, cleaned and merged to create final datasets
- Climate_Data_Cleaning_Notebook: loaded raw PRISM data, cleaned to create final dataset

#### Data Exploration
- AppleData_Exploration: uses clean data, creates graphical representations of the apple data
- Climate_Data_EDA_Notebook: uses clean data, creates graphical representations of climate (PRISM) data

#### Modeling
- Model_LogisticRegression: logistic regression model for percent of apple production utilized (all or not all) 
- Prophet_Model: Facebook Prophet Model for yield per tree using weather data as features

## Sources
Apple Data:
- https://quickstats.nass.usda.gov/
- https://www.nass.usda.gov/Statistics_by_State/Washington/Publications/Fruit/2017/FT2017.pdf

Facebook Prophet Model Resources:
-  https://facebook.github.io/prophet/
-  https://towardsdatascience.com/generalised-additive-models-6dfbedf1350a
- https://nbviewer.org/github/nicolasfauchereau/Auckland_Cycling/blob/master/notebooks/Auckland_cycling_and_weather.ipynb
- https://machinelearningmastery.com/time-series-forecasting-with-prophet-in-python/
