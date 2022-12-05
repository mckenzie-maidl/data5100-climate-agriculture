# data5100-climate-agriculture
Project repository for DATA 5100 (Foundations of Data Science) for the MS Data Science program at Seattle University.

Fall 2022 | Alexander Churchill, Malia Kortez, McKenzie Maidl, Yootaek Oh

## Problem Statement
ADD!

## Repository Contents

### Data

#### Raw Data
Contains data files on climate and apples before they were cleaned.

##### Apple Data
The following dataset is from the United States Department of Agriculture Census of Agriculture for Washinton state (multiple years, collected from PDF formats of census reports):
- apple_production_farms: apple trees and farm counts by year for Washington state

The following datasets are each from the United States Department of Agriculture National Agricultural Statistics Service: 
- USDA_NASS_WA-apples_1889-2010: apple production data for Washington state, 1889 - 2010
- WA_apple_production_2007_2022: apple production data for Washington state, 2007 - 2022
- WA_apple_yields_lb_acre_2007-2021: apple yields data for Washington state, 2007 - 2021
- WA_apples_bearing_2007_2021: apple bearing acres data for Washington state, 2007 - 2021
- WA_apple_price_1909_2021: apple price data for Washington state, 2007 - 2021
- WA_apples_utilized_production_2007_2021: apple utilized production data for Washington state, 2007 - 2021

#### Cleaned Data
Contains cleaned and merged versions of the raw data files.

- WA_apples_1889_2021: merged apple data from 1889 - 2021
- apples_1970: subset of needed columns, 1970 - 2021
- apples_years: a merged apple/climate dataset used in modeling

#### GIS Data
Contains water and county shape data for Washington state.

### Colab Notebooks
These notebooks contain the code that was used for this project.

#### Data Cleaning
- AppleData_Cleaning: loaded raw apple data, cleaned and merged to create final datasets

#### Data Exploration
- AppleData_Exploration: uses clean data, creates graphical representations of the apple data

#### Modeling
- Model_LogisticRegression: logistic regression model for percent of apple production utilized (all or not all) 
