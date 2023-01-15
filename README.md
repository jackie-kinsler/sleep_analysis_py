## Fitbit Data Analysis 

This analysis aims to understand if sleep duration or quality are correlated with Fitbit physical stats (like steps, heartrate, active minutes, etc.).

Tools and libraries: 
- **pandas** offers data structures for data analysis (dataframes, aka tables), as well as basic data manipulation 
- **matplotlib** is used for plotting 

### Data Import  : [`import_data.ipynb`](https://github.com/jackie-kinsler/sleep_analysis_py/blob/master/import_data.ipynb)
A complete archive of Fitbit account data data was exported from Fitbit's website. Instructions on that are [here](https://help.fitbit.com/articles/en_US/Help_article/1133.htm).

The raw data is a combination of JSON files and .csv files. 

All of the import code is in [`import_data.ipynb`](https://github.com/jackie-kinsler/sleep_analysis_py/blob/master/import_data.ipynb). 
After importing the raw data, the data is saved to the `data/` directory. 

I am not including the `data/` directory as it is rather large. 

### Data Cleaning  : [`clean_and_explore.ipynb`](https://github.com/jackie-kinsler/sleep_analysis_py/blob/master/clean_and_explore.ipynb)

There are two main portions to the data cleaning: 

1) General cleaning operations
- handling nulls
- ensuring no duplictes
- etc. 
2) Exploring the data with plots, and investigating outliers 

After the data is cleaned, it is saved to the `cleaned_data/` directory. 

### Data Analysis  : [`sleep_analysis.ipynb`](https://github.com/jackie-kinsler/sleep_analysis_py/blob/master/sleep_analysis_py.ipynb)

For the analysis, all of the data is joined into one table.  
Then, a correlation matrix is performed to understand if any of the physical stats are correlated with sleep duration or sleep quality. 

Sedentary minutes (time spent stationary for 10 or more minutes) had the highest R value at 0.47. 

In general, the more sedentary minutes, the shorter the sleep duration. 

**Additional Analysis**  
In April 2022 I took a career break to hike/climb/ski full time. There is a short section to discover what impact this had on my activity, sleep, and heartrate.
