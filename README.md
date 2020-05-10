# COVID-19 and Urban Air Pollution
The public health crisis caused by the Novel Coronavirus (COVID-19) prompted governments worldwide to restrict human movement in a bid to limit the spread of the respiratory disease. Since the outbreak in March 2020 in the United States, many states and municipalities have issued stay-at-home orders, and economic activity has been largely reduced to essential services only. The unprecedented restriction on economic activity has led to a significant drop in traffic volume, factory production, and other sources widely attributed to urban air pollution, leading to a substantial improvement in air quality in major U.S. cities.

In this project, we analyze the relationship between the severity of COVID-19 outbreak and air quality in New York City using daily time series of air pollution, vehicle throughput on MTA bridges and tunnels, and industrial manufacturing activity. We find traffic volume and manufacturing activity are positively correlated with EPA Air Quality Index (AQI), and confirmed COVID-19 cases negatively correlated.

## Reproducing the Notebook with Binder
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tianrunw/big-data-air-pollution/master)

We use Jupyter Notebook for data analysis in this project, see `project/covid19_air_pollution.ipynb`. All data files are located in `project/data` directory.

We offer two solutions for reproducibility, the first is through [Binder](https://mybinder.org/). Binder automatically copies and runs this repo on a cloud-hosted Jupyter Notebook environment, installing the dependencies listed in `requirements.txt` beforehand. To run this repo on Binder interactively, click on the Binder badge above. Note that the startup takes a few minutes as Binder builds a docker image and deploys it in the background.

The second is the traditional local environment, before running the notebook on your local machine, please install the dependencies listed in `requirements.txt`. In addition, we also included an HTML version of the notebook in root directory, see `covid19_air_pollution.html`.

## Major Findings
For a high-level overview of this project, see `project_presentation_group4.pdf` in root directory.

In this research project, we found that COVID-19 confirmed cases are negatively correlated with EPA Air Quality Index (better air quality) in New York metropolitan area as people stay home and traffic-related pollution decreased. Among the major air pollutants in New York City, we find that PM2.5 is positively correlated to traffic volume, with a reduction in ground traffic leading to a drop in PM2.5 emission. On the other hand, Ozone pollution is negatively correlated to traffic volume possibly due to the Weekend Effect as we observed an increase in Ozone concentration during the COVID-19 shutdown. However, as PM2.5 has a greater contribution to AQI, the overall air quality did improve as less vehicles are found on the ground.

Linear regression models suggest strong collinearity between confirmed cases, traffic volume, and energy demand, due to confirmed cases tend to depress local economic activities. We find that traffic volume and energy demand load positively on AQI, and confirmed cases loads negatively. Traffic volume tends to have the highest statistical significance with t-stat generally greater than 2, with the other two independent variables generally not significant except in the case of Ozone concentration.

We simulated possible air quality outcomes depending on what percentage of the economy reopens, and found that a 50% recovery of normal traffic is related to an increase in AQI to 44.15, and a full recovery of normal traffic will lead to an AQI value of 49.52, using median projections.

A major challenge we faced in data analysis is the reconciliation of the strong correlation between confirmed cases and traffic volume and manufacturing activity. As confirmed cases directly cause governments to shut down the economy and subsequently traffic and industrial activity, we must often drop confirmed cases from regression models as most of the variance in air quality is explained by traffic volume and manufacturing activity, causing confirmed cases to have a low statistical significance.

## Data Sources
See `datasets-used.csv` for a detailed description of data sources, and `project/data/README.md` for description of specific data files.

- Johns Hopkins CSSE COVID-19 Data Repository: [csse_covid_19_time_series](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series)

- New York City COVID-19 Data Repository: https://github.com/nychealth/coronavirus-data

- U.S. Environmental Protection Agency (EPA): [Air Quality Index Daily Values Report](https://www.epa.gov/outdoor-air-quality-data/air-quality-index-daily-values-report)

- Open NY (New York State): [Hourly Traffic on MTA Bridges and Tunnels](https://data.ny.gov/Transportation/Hourly-Traffic-on-Metropolitan-Transportation-Auth/qzve-kjga)

- Chicago Mercantile Exchange (CME): [Daily Settlement of WTI Crude Oil Futures](https://www.cmegroup.com/trading/energy/crude-oil/light-sweet-crude.html)
