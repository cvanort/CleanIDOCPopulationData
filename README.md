# Clean and Combine IDOC Population Data

IDOC publishes population data sets which consist of each person housed in a state prison each quarter and information about them, such as their demographics, the type of crime they're being held for, the date on which they were apprehended, etc. The data sets are .xls files, but the titles, URLs, and data within each data set differ and need to be cleaned. This script combines all population data sets and makes the information within them consistent.

The population data sets can be found here: https://www2.illinois.gov/idoc/reportsandstatistics/Pages/Prison-Population-Data-Sets.aspx

Specifically, the script does the following:
* Reads in the data sets
* Combines the data sets, labeling each with the last date of the month on which it was published
* Combines data columns with same information but different names
* Transforms the dates into dates, where possible
* Calculates recidivism: the sentence number for each individual
* Cleans and categorizes the sentencing counties
* Splits the truth-in-sentencing values into percents and descriptions
* Cleans and categorizes the holding offenses
* Cleans the parent institution names
* Cleans and categorizes the admission type
* Transforms old admission types into the new ones
* Determines whether an individual is eligible for earned discretionary sentencing credits
