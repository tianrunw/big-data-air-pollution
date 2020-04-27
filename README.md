# COVID-19 and Urban Air Pollution
The public health crisis caused by the Novel Coronavirus (COVID-19) prompted governments worldwide to restrict human movement in a bid to limit the spread of the respiratory disease. Since the outbreak in March 2020 in the United States, many states and municipalities have issued stay-at-home orders, and economic activity has been largely reduced to essential services only. The unprecedented restriction on economic activity has led to a significant drop in traffic volume, factory production, and other sources widely attributted to urban air pollution, leading to a substantial improvement in air quality in major U.S. cities.

In this project, we analyze the relationship between the severity of COVID-19 outbreak in a city and the improvement of air quality. We will primarily focus our analysis on the experience of New York City, due to the quality and availability of its high-frequency data on ground traffic, air pollution and COVID-19 case count.


## Team Memebers
- Raymond Dee (rmd377@nyu.edu)
- Jonathan Pun (jp5474@nyu.edu)
- Tianrun Wang (tw969@nyu.edu)


## Reproducing the Notebook with Binder
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tianrunw/big-data-air-pollution/master)

We use Jupyter Notebooks for data analysis in this project, found in the main `project` directory. All data files are located in `project/data` folder.

We offer two solutions for reproducibility, the first is through [Binder](https://mybinder.org/). Binder automatically copies and runs this repo on a cloud-hosted Jupyter Notebook environment, installing the dependencies listed in `requirements.txt` beforehand. To run this repo on Binder interactively, click on the Binder badge above.

The second is the traditional local environment, before running the notebook on your local machine, please install the dependencies listed in `requirements.txt`. Furthermore, we are working on building a ReproZip package for this repo as well, which is coming soon.


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
See `datasets-used.csv` for detailed description of data sources, and `project/data/README.md` for description of specific data files.

- Johns Hopkins CSSE COVID-19 Data Repository
    - [csse_covid_19_time_series](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series)

- New York City COVID-19 Data Repository
    - https://github.com/nychealth/coronavirus-data

- U.S. Environmental Protection Agency (EPA)
    - [Air Quality Index Daily Values Report](https://www.epa.gov/outdoor-air-quality-data/air-quality-index-daily-values-report)

- Open NY (New York State)
    - [Hourly Traffic on MTA Bridges and Tunnels](https://data.ny.gov/Transportation/Hourly-Traffic-on-Metropolitan-Transportation-Auth/qzve-kjga)

- Bureau of Transportation Statistics (Department of Transportation)
    - [Airline On-Time Statistics (Departures)](https://www.transtats.bts.gov/ONTIME/Departures.aspx)

- Chicago Mercantile Exchange (CME)
    - [Daily Settlement of WTI Crude Oil Futures](https://www.cmegroup.com/trading/energy/crude-oil/light-sweet-crude.html)
