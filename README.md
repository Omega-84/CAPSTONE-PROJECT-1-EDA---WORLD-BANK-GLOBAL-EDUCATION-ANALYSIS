# AlmaBetter EDA Capstone Project 1 Worldbank EdStats

This project is a part of the [AlmaBetter Premium Program](https://www.almabetter.com/) , Banglore/Bengaluru ,Karnataka , India

#### -- Project Status: [Completed]

## Project Summary :
#### About the Dataset :
We are provided with a dataset  named World Bank EdStats that contains 4000 indicators describing education access(primary, vocational and tertiary), progression, literacy, teacher, population etc. 

The World Bank is an international financial institution which provides monetary assistance to governments of low and middle countries for socio-economic development. Each year, the World Bank collects various statistics through international statistical communities and globally coordinated programs to monitor the growth and progress of various economies. 

#### Problem Statement : 
We were provided with 5 datasets and asked to find insights and trends for different groups of countries and come up with a rough estimate as to which countries are alike and which are dissimilar.

#### Approach taken :
The idea of the project is to analyze the data and mark the variation of indicators across the globe, and also group the countries according to their similarities and differences.

#### Insights from exploring the Data :
From the BRICS countries, we can conclude that the populations of India and China showed growth over the years, with India’s growth rate overtaking China’s after the 2000s.
India’s pre-primary and tertiary enrollment percentage is pretty low when compared to other BRICS countries, but increasing from 1995.
The mortality rate has dropped for every country, the highest drop being observed in India, where more focus was laid on education over the years .
Immigration in USA from 1990-2000 increased the population growth rate for that 10-yr time period
The countries having the highest drop-out rate affected the GNI per capita for those countries

#### Challenges faced:
It was very challenging to completely understand the data and to comprehend the relevance of each CSV file 
As the percentage of missing data was huge, it took a lot of effort to decide on the final data to keep for analysis
Filtering out the best indicators from 3700 indicators to keep for analysis
Deciding on the set of countries to work based on economy and geography

#### Future scope of work:
Working out on Top European powers and compare their positions based on different indicators
Considering the amount of indicators in the data, if we dig deep enough, various micro trends can be unearthed, which we were not able to extensively cover during this short duration.
This dataset can also be used to measure compensation of teachers, if we are to advise the education ministry on management of funds.
Learning Assessment Indicators for Mathematics and Science can be used to predict populations that tend to have a knack for technology.


### Data Visualization Methods Used
* Time Series Lne graphs
* Pie Chart Plots
* World Map Chloropeth Plots
* Heat maps
* Size-Heat maps

### Python Libraries used
For Graphing : 
* Matplotib
* Seaborn 
* heatmapz
* Dash-Plotly

Datawrangling : 
* Numpy
* Pandas
* Json
* pprint - Pretty Printer 


## Getting Started

1. Clone this repo (for help see this [tutorial](https://help.github.com/articles/cloning-a-repository/)).
2. Raw Data is being kept [here](https://drive.google.com/drive/folders/1zbIOG82jvDXavYuGazysc0j89GRzWz__?usp=sharing) within GDrive
    


## The Structure of the main IPYNB notebook :

* Initial Library imports 
* Exploring File : EdStatsCountries.csv
  * Reading data and exploring which columns are necessary
  * Geographic and Economic Special- Macro- country codes
  * Grouping countries by Geographic and Economic groups ( Size-Heatmap )

* Exploring File : EdStatsSeriies.csv
  * Reading data and exploring which columns are necessary
  * Understanding the indicator series : 
    * What about what topics are these indicators 
    * How many indicators per topic
  * Utility Function : get_indicator_details() : 
    * This function return the details of an indicator as dictionary , 
    * useful for retrieving definition and name during plots

* Exploring File : EdStatsData.csv
  * Reading data and exploring which columns are necessary
  * Removing Columns for Future Years , 
  * Removing Rows which are Empty
  * Understanding the availability of Data for each Year
    * Both before and after cleaning with Bar Plots

* Utility Function : Comparative analysis
  * get_pivot_similiarity():
  * this function takes two countries as an input and calculates how similar they are based on all available indicators , from 1970 to 2015

* Utility Function for full Report Generation 
  * generate_report():
  * This function takes a list of countries and one indicator as Input 
  * It generates multiple different plot so that we can instantly get an idea of what is going on for that indicator
  * the plots generated include :
    * Line graph of values of that indicator for all countries in the list passed , over time from 1970 to 2015
    * Pie Chart Plot for those counties for one particular year passed as input 
    * Similarity Heat Map - for visualizing which countries are more similar to each other , for each country pair inside the list of countries
      * this function is based on the Utility function for Comparative analysis called : get_pivot_similiarity
      * the output generated is similar to that of a correlation plot .

* World Map Visualization : 
  * Dash Plotly library used for making a world map chloropleth plot 
  * Indicators such as Population , Population Growth and GDP(PPP) are visualized in this section

* Case Study : BRICS Countries : 
  * BRICS Countries : Brazil Russia India China South-Africa
  * Study of Population Growth 
  * Study of How the expenditure on education impacts the education outcomes
  * Study of correlation between Educated, GDP and  Mortality 

* Case Study : Comparison between Education in India and America
  * Study of Primary and Primary and Tertiary Education Outcomes and Expenditures
  * Comparative study of Drop-Out rate 




## Contributing Team Members:

|Name     |  Email   | 
|---------|-----------------|
|Saifuddin Raja(https://github.com/saif-raja) |     saifuddin.raja24@gmail.com    |
|Varun Nayyar(https://github.com/saif-raja) |     nayyar.varun84@gmail.com    |
|Fahad Mehfooz(https://github.com/saif-raja) |    fahad.mehfoooz@gmail.com    |
|Shubham Bareja(https://github.com/saif-raja) |     sbshubham23@gmail.com    |
|Pooja Rana(https://github.com/saif-raja) |     rana.pooja800@gmail.com    |
|Anirudh Upadhyay(https://github.com/saif-raja) |     anirudh31ajm@gmail.com    |
