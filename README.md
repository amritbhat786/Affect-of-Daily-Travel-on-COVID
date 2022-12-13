# data-512-project-common-analysis

**DATA 512: Human-Centered Data Science**


[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/amritbhat786/Human-Cenetered-Data-Science/blob/main/LICENSE)

During the last three years we all have been experiencing a global pandemic. This has been tragic and disruptive to many countries and has taken a deep personal toll on many individuals and their families. 

One aspect that has been hard to miss in the last three years is the datafication of the pandemic. That is, many aspects of the individual toll of the pandemic have been collected, aggregated and re-represented as data. This datafication gives us the privilege to examine the pandemic from potentially many different perspectives to understand how it has changed lives and how it has changed society. To be honest, we are actually at the very beginning of understanding and comprehending these impacts.

The goal of this Course Project is to begin taking a look at some of the social aspects of the pandemic by conducting a human centered data science analysis of some available COVID-19 data.


### Data Source:

The data for this project is extracted has different aspects and way of collection. One source is CDC for county specific information, other John Hopkins with confirmed cases data shared on Kaggle and other is New York Times Survey data.

Dataset Sources The RAW_us_confirmed_cases.csv file from the Kaggle repository of John Hopkins University COVID-19 data. This data is updated daily and recent version is used for analysis The CDC dataset of masking mandates by county. Note that the CDC stopped collecting this policy information in September 2021. The New York Times mask compliance survey data.


- [RAW US confirmed cases CSV file from the Kaggle repository of John Hopkins University COVID-19 data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university)
 This data is updated daily. There are no ethical considerations I feel we have to consider with this dataset, as these are the actual cases that were reported publicly. Licensed under Attribution 4.0 International (CC BY 4.0). Overall, this dataset will contain the daily COVID case count, which will act as our dependent variable in the analysis. **THIS DATA IS NOT INCLUDED IN THIS REPOSITORY AS THE FILESIZE WAS TOO LARGE. PLEASE DOWNLOAD IT DIRECTLY FROM THE LINK LOCALLY**

| Column name     | Description               |
| --------------- | ------------------------- |
| Province\_State | Province or state         |
| Admin2          | Country                   |
| UID             | Unique identifier         |
| iso2            | Unused geography code     |
| iso3            | Unused geography code     |
| code3           | Unused geography code     |
| FIPS            | Unique 5-digit identifier |
| Lat             | Latitude                  |
| Long\_          | Longitude                 |


- [Trips by Distance - Bureau of Transportation Statistics] (https://data.bts.gov/Research-and-Statistics/Trips-by-Distance/w96p-f2qv)  
This dataset is used to understand daily travel behaviors of people in Cook County, Illinois. The dataset summarizes how many people are staying at home during the COVID-19 pandemic and how far people are traveling when they don’t stay home. It consists of 22 columns out of which I felt 16 relevant for our analysis. This dataset is licensed under [U.S. Government Works] (https://www.usa.gov/government-works). I couldn’t find any information on Terms of Use, however. Data Description of this data can be found in the above link. **THIS DATA IS NOT INCLUDED IN THIS REPOSITORY AS THE FILESIZE WAS TOO LARGE. PLEASE DOWNLOAD IT DIRECTLY FROM THE LINK LOCALLY**


- [CDC dataset of masking mandates by county](https://www.google.com/url?q=https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i&sa=D&source=docs&ust=1667551398820431&usg=AOvVaw21FMdhJyclbjdmZW98QUbK) **THIS DATA IS NOT INCLUDED IN THIS REPOSITORY AS THE FILESIZE WAS TOO LARGE. PLEASE DOWNLOAD IT DIRECTLY FROM THE LINK LOCALLY**

| Column name                       | Description               |
| --------------------------------- | ------------------------- |
| State\_Tribe\_Territory           | State or tribe name       |
| County\_Name                      | County name               |
| FIPS\_State                       | Numeric state identifier  |
| FIPS\_County                      | Numeric county identifier |
| date                              | YYYY-MM-DD format         |
| order\_code                       | Order type                |
| Face\_Masks\_Required\_in\_Public | Boolean identifier        |
| Source\_of\_Action                | Authority                 |
| URL                               | URL                       |
| Citation                          | Citation                  |


- [The New York Times mask compliance survey data](https://github.com/nytimes/covid-19-data/tree/master/mask-use) 

| Column name | Description                                                     |
| ----------- | --------------------------------------------------------------- |
| COUNTYFP    | Numeric state and county identifier                             |
| NEVER       | Percentage of respondants responding "never" wearing masks      |
| RARELY      | Percentage of respondants responding "rarely" wearing masks     |
| SOMETIMES   | Percentage of respondants responding "sometimes" wearing masks  |
| FREQUENTLY  | Percentage of respondants responding "frequently" wearing masks |
| ALWAYS      | Percentage of respondants responding "always" wearing masks     |


### Intermediate data files
- Commons-Analysis/data/daily_new_cases_cook_county.csv - Combined data after merging Masking mandate and total cases dataset. 

| Column name     | Description               |
| --------------- | ------------------------- |
| date            | YYYY-MM-DD format         |
| confirmed_cases | Total confirmed cases     |
| mask_required   | Flag variable mask mandate|
| cases           | Daily Active Cases        |
