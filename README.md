# Bitcoin-Price-Prediction
Used historical data on the price of Bitcoin, along with data from Wikipedia about edits to the Bitcoin page.  Merged and combined this data, then used it to train a random forest model that will tell us if Bitcoin prices will increase or decrease tomorrow. Then switch to an XGBoost model and better predictors to improve accuracy.


**Project Steps**

* Load in data
* Clean and merge data
* Create an initial machine learning model and estimate accuracy
* Switch to a more powerful model and improve our predictors

File overview:

* `prediction.ipynb` - a Jupyter notebook that contains the code to predict Bitcoin prices
* `sentiment.ipynb` - a Jupyter notebook that creates our wikipedia edit dataset.

# Local Setup

## Installation

To follow this project, please install the following locally:

* JupyerLab
* Python 3.8+
* Python packages
    * pandas
    * yfinance
    * scikit-learn
    * xgboost
    * mwclient
    * transformers

## Data

Computing the Wikipedia edit data takes time.  It can be faster to use the version that's already been generated.  It's in this repository, and called `wikipedia_edits.csv`.  Feel free to download and use the file.  You can also get it from [here](https://drive.google.com/uc?export=download&id=1XwJZ07bl2u-62yRMqV_emJGEXCI1u8dl).

We'll be downloading the Bitcoin price data using the `yfinance` package as part of the project.

## Running

First, run the code in `sentiment.ipynb` to generate a new Wikipedia edits dataset.  The dataset committed in the repo is old, and this will get the edits up to the present day.

Second, run the code in `prediction.ipynb`.  By default, this will load data from an existing `btc.csv` file.  Removing that code will ensure that it downloads the newest data from Yahoo Finance.

