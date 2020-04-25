# COVID-19 and Urban Air Pollution
The public health crisis caused by the Novel Coronavirus (COVID-19) prompted governments worldwide to restrict human movement in a bid to limit the spread of the respiratory disease. Since the outbreak in March 2020 in the United States, many states and municipalities have issued stay-at-home orders, and economic activity has been largely reduced to essential services only. The unprecedented restriction on economic activity has led to a significant drop in traffic volume, factory production, and other sources widely attributted to urban air pollution, leading to a substantial improvement in air quality in major U.S. cities.

In this project, we analyze the relationship between the severity of COVID-19 outbreak in a city and the improvement of air quality. We will primarily focus our analysis on the experience of New York City, due to the quality and availability of its high-frequency data on ground traffic, air pollution and COVID-19 case count.


## Team Memebers
- Raymond Dee (rmd377@nyu.edu)
- Jonathan Pun (jp5474@nyu.edu)
- Tianrun Wang (tw969@nyu.edu)


## Major Points of Analysis
- How did traffic change in response to the number of confirmed COVID cases?
    - Did traffic volumes drop before a city went into lockdown officially?
    - Did traffic volumes increase as people expected to be quarantined and rushed out to do last-minute tasks?

- How has air pollution changed in select metro areas in response to lockdowns?
    - Currently the best data for both traffic and air pollution exists for NYC though we are searching for other major cities

- How have the major sources of air pollution changed in response to COVID?
    - Traffic is the major source of pollution in NYC


## Data Modeling and Predictive Analysis
- Predictive analysis using linear regression on time series
- Regress traffic volume on Covid-19 case count to analyze the relationship between the severity of epidemic in a locality between traffic activity
- Regress air quality on traffic activity to analyze the relationship between traffic volume and air quality


## Data Sources
- U.S. Environmental Protection Agency (EPA)
    - https://www.epa.gov/outdoor-air-quality-data
    - https://aqs.epa.gov/aqsweb/documents/data_api.html

- Air Now
    - https://www.airnow.gov/

- Hourly Traffic MTA Bridges and Tunnels (New York State)
    - https://data.ny.gov/Transportation/Hourly-Traffic-on-Metropolitan-Transportation-Auth/qzve-kjga

- Johns Hopkins Covid-19 Data
    - https://github.com/CSSEGISandData/COVID-19
