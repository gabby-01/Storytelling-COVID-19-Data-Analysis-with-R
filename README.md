# Introduction
The COVID-19 Data Analysis project utilizes R programming language. The project analyzes the "Coronavirus (COVID-19) Deaths" dataset obtained from the [Our World in Data](https://ourworldindata.org/covid-deaths). Our World in Data is a public resource that provides open access to its data for the public and policymakers.

# Aim & Objectives
**Aim**: To analyze the COVID-19 dataset and gain insights into the current trends and patterns of the disease across different countries in order to provide meaningful recommendations, policies, interventions, and strategies aimed at reducing the impact of the disease and protecting public health.

**Objectives**:
* To conduct data exploration to understand the structure of the dataset.
* To perform data preprocessing to clean, transform, and enhance the quality of the data for the improvement of accuracy in further analysis.
* To conduct data visualisation on the generated questions of community problems of COVID-19.
* To provide a comprehensive interpretation of the visualisations for each question by translating data analyses into understandable terms.

# Dataset
* **Dataset**: [owid-covid-data](https://docs.google.com/spreadsheets/d/1y54iWRwsC_IvG4-lsCgjU4aW8DrSKVf_/edit?usp=share_link&ouid=103544631015385382299&rtpof=true&sd=true)
* **Description**: The dataset provides information on the number of COVID-19 deaths reported worldwide. It contains 302751 rows and 67 columns from the duration 1st Jan 2020 - 14th Apr 2023. 

The following descriptions of the 67 variables in the dataset:

|No|Variables|Description|
|--|---------|-----------|
|1|iso_code|Three-letter ISO code for the country/region| 
|2|continent|Continent in which the country/region is located|
|3|location|Name of the country/region|
|4|date|Date in format yyyy/mm/dd|
|5|total_cases|Total number of confirmed COVID-19 cases|
|6|new_cases|Number of new confirmed COVID-19 cases|
|7|new_cases_smoothed|7-days rolling average of the number of new confirmed COVID-19 cases|
|8|total_deaths|Total number of COVID-19 deaths|
|9|new_deaths|The number of new COVID-19 deaths|
|10|new_deaths_smoothed|7-days rolling average of the number of new COVID-19 deaths|
|11|total_cases_per_million|Total number of confirmed COVID-19 cases per million people|
|12|new_cases_per_million|Number of new confirmed COVID-19 cases per million people|
|13|new_cases_smoothed_per_million|7-days rolling average of the number of new confirmed COVID-19 cases per million people|
|14|total_deaths_per_million|Total number of COVID-19 deaths per million people|
|15|new_deaths_per_million|Number of new COVID-19 deaths per million people|
|16|new_deaths_smoothed_per_million|7-days rolling average of the number of new COVID-19 deaths per million|
|17|reproduction_rate|Estimated average number of people who will contract COVID-19 from a single infected person|
|18|icu_patients|Number of COVID-19 patients who are currently in an intensive care unit (ICU)|
|19|icu_patients_per_million|Number of COVID-19 patients who are currently in an intensive care unit (ICU) per million people|
|20|hosp_patients|Total number of COVID-19 patients who are currently in a hospital|
|21|hosp_patients_per_million|Number of COVID-19 patients who are currently in a hospital per one million people|
|22|weekly_icu_admissions|Number of COVID-19 patients who are admitted to an intensive care unit (ICU) during a specific week|
|23|weekly_icu_admissions_per_million|Number of COVID-19 patients who were admitted to an intensive care unit (ICU) during a specific week per one million people|
|24|weekly_hosp_admissions|Number of COVID-19 patients who were admitted to a hospital during a specific week|
|25|weekly_hosp_admissions_per_million|Number of COVID-19 patients who were admitted to a hospital during a specific week per one million people|
|26|total_tests|Total number of COVID-19 tests that have been administered|
|27|new_tests|Number of new COVID-19 tests that have been administered|
|28|total_tests_per_thousand|Total number of COVID-19 tests that have been administered per one thousand people|
|29|new_tests_per_thousand|Number of new COVID-19 tests that have been administered per one thousand people|
|30|new_tests_smoothed|7-days rolling average of the number of new COVID-19 tests that have been administered|
|31|new_tests_smoothed_per_thousand|7-days rolling average of the number of new COVID-19 tests that have been administered per one thousand people|
|32|positive_rate|The proportion of COVID-19 tests that have returned positive results|
|33|tests_per_case|The number of COVID-19 tests that have been administered per confirmed case of COVID-19|
|34|tests_units|The units used to measure COVID-19 testing|
|35|total_vaccinations|The total number of COVID-19 vaccine doses that have been administered|
|36|people_vaccinated|The total number of people who have received at least one dose of a COVID-19 vaccine|
|37|people_fully_vaccinated|The total number of people who have received all required doses of a COVID-19 vaccine|
|38|total_boosters|The total number of COVID-19 vaccine booster doses that have been administered|
|39|new_vaccinations|The number of new COVID-19 vaccine doses that have been administered|
|40|new_vaccinations_smoothed|7-days rolling average of the number of new COVID-19 vaccine doses that have been administered|
|41|total_vaccinations_per_hundred|Total number of COVID-19 vaccination doses administered per 100 people|
|42|people_vaccinated_per_hundred|Total number of people who have received at least one dose of a COVID-19 vaccine per hundred people|
|43|people_fully_vaccinated_per_hundred|Total number of people who have received all required doses of a COVID-19 vaccine per hundred people|
|44|total_boosters_per_hundred|Total number of COVID-19 booster doses administered per 100 people|
|45|new_vaccinations_smoothed_per_million|7-days rolling average of the number of new COVID-19 vaccine doses that have been administered per million people|
|46|new_people_vaccinated_smoothed|7-days rolling average of the number of new people who have received at least one dose of a COVID-19 vaccine|
|47|new_people_vaccinated_smoothed_per_hundred|7-days rolling average of the number of new people who have received at least one dose of a COVID-19 vaccine per 100 people|
|48|stringency_index|Composite measure of the strictness or severity of COVID-19 containment policies|
|49|population_density|Number of people per square kilometre of land area|
|50|median_age|Median age of the population|
|51|aged_65_older|The percentage of the population aged 65 years and older|
|52|aged_70_older|The percentage of the population aged 70 years and older|
|53|gdp_per_capita|Gross Domestic Product (GDP) per capita in current US dollars|
|54|extreme_poverty|The percentage of the population living in extreme poverty|
|55|cardiovasc_death_rate|The age-standardized death rate from cardiovascular disease|
|56|diabetes_prevalence|The percentage of the population aged 20-79 years with diabetes|
|57|female_smokers|The percentage of women who smoke|
|58|male_smokers|The percentage of men who smoke|
|59|handwashing_facilities|The percentage of the population with access to basic handwashing facilities|
|60|hospital_beds_per_thousand|The number of hospital beds per thousand population|
|61|life_expectancy|The life expectancy at birth of the population|
|62|human_development_index|Rank countries based on their levels of human development|
|63|population|The total population in a particular location|
|64|excess_mortality_cumulative_absolute|The absolute number of excess deaths in a location since the beginning of the pandemic|
|65|excess_mortality_cumulative|The percentage increase in mortality in a location since the beginning of the pandemic|
|66|excess_mortality|The percentage increase in mortality in a location during a particular period of time|
|67|excess_morality_cumulative_per_million|The number of excess deaths per million people in a location since the beginning of the pandemic|

# Processed Dataset
* **Dataset**:  [owid-covid-data (processed data)](https://docs.google.com/spreadsheets/d/1ErhY8Z2vigtF4S-cP_INl90mrSTSTPge/edit?rtpof=true#gid=1188884259)
* **Description**: The dataset has been meticulously processed, involving data reduction, data cleaning, and data transformation techniques. By undergoing these procedures, the dataset is now optimized for accurate and meaningful analysis.

The processed dataset consisted of the following 30 variables:

|No|Variables|Description|
|--|---------|-----------|
|1|continent|Continent in which the country/region is located|
|2|country|Name of the country/region|
|3|date|Date in format yyyy/mm/dd|
|4|total_cases|Total number of confirmed COVID-19 cases|
|5|new_cases|Number of new confirmed COVID-19 cases|
|6|new_deaths|The number of new COVID-19 deaths|
|7|reproduction_rate|Estimated average number of people who will contract COVID-19 from a single infected person|
|8|new_tests|Number of new COVID-19 tests that have been administered|
|9|positive_rate|The proportion of COVID-19 tests that have returned positive results|
|10|tests_per_case|The number of COVID-19 tests that have been administered per confirmed case of COVID-19|
|11|people_vaccinated|The total number of people who have received at least one dose of a COVID-19 vaccine|
|12|people_fully_vaccinated|The total number of people who have received all required doses of a COVID-19 vaccine|
|13|total_boosters|The total number of COVID-19 vaccine booster doses that have been administered|
|14|new_vaccinations|The number of new COVID-19 vaccine doses that have been administered|
|15|stringency_index|Composite measure of the strictness or severity of COVID-19 containment policies|
|16|population_density|Number of people per square kilometre of land area|
|17|median_age|Median age of the population|
|18|aged_65_older|The percentage of the population aged 65 years and older|
|19|aged_70_older|The percentage of the population aged 70 years and older|
|20|gdp_per_capita|Gross Domestic Product (GDP) per capita in current US dollars|
|21|extreme_poverty|The percentage of the population living in extreme poverty|
|22|cardiovasc_death_rate|The age-standardized death rate from cardiovascular disease|
|23|diabetes_prevalence|The percentage of the population aged 20-79 years with diabetes|
|24|female_smokers|The percentage of women who smoke|
|25|male_smokers|The percentage of men who smoke|
|26|handwashing_facilities|The percentage of the population with access to basic handwashing facilities|
|27|hospital_beds_per_thousand|The number of hospital beds per thousand population|
|28|life_expectancy|The life expectancy at birth of the population|
|29|human_development_index|Rank countries based on their levels of human development|
|30|population|The total population in a particular location|

