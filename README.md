# Avalanche Canada: Web Scraping and Analysis

These notebooks work through scraping [avalanche.ca](https://avalanche.ca/map) for historical avalanche rating data by region and elevation, and then run some analyses to identify patterns that emerge.

___
## How to run code
* web_scrape_avalanche.ipynb: Scrapes [avalanche.ca](https://avalanche.ca/map) and structures data by region for analysis
* investigate.ipynb: Runs analysis on the data
* region_boundaries.ipynb: Defines the avalanche region boudaries for use in investigate.ipynb

___
## Findings

The code is set up to scrape and analyze regions across Western Canada with a sufficient time series of ratings.

<img src= "https://github.com/andersonsam/avalanche_canada/blob/main/Figures/regions.png" width=50% >

Above-treeline rating time series can be clustered to see which regions are most similar at these elevations, with interesting regional patterns emerging.

<img src= "https://github.com/andersonsam/avalanche_canada/blob/main/Figures/above_treeline_clusters_space.png" width=50% >

<img src= "https://github.com/andersonsam/avalanche_canada/blob/main/Figures/above_treeline_clusters_time.png" width=50% >

Each region can be characterized according to its mean avalanche rating, variance of rating through time, and gradient of rating across elevation (e.g. how much higher is the above-treeline rating vs the below-treeline rating?).  For example the lower mainland has a relatively low rating on average, but with high variance in time and across elevation (e.g. above-treeline ratings are much higher than below-treeline ratings).

<img src= "https://github.com/andersonsam/avalanche_canada/blob/main/Figures/region_characteristics.png" width=100% >

In the space of rating gradient across elevation vs mean rating, interesting patterns appear!  Note the high-mean-high-gradient northwest coast, high-mean-low-gradient cariboo/columbia/purcells.

<img src= "https://github.com/andersonsam/avalanche_canada/blob/main/Figures/gradient_vs_mean.png" width=50% >

<img src= "https://github.com/andersonsam/avalanche_canada/blob/main/Figures/gravient_vs_mean_clusters_space.png" width=50% >

___
## Requirements

Outside of Python 3.6 and some standard scientific python packages (e.g. numpy, pandas, scikit-learn), you will need [Chromedriver](https://chromedriver.chromium.org/) installed for webscraping.
