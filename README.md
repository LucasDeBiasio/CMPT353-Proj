
# Analyzing Canada’s Provincial Life Satisfaction and Sentiment in Provincial Subreddit Submissions

This repo contains the final project for CMPT 353 by [Jocelyn Tandrea](#authors) and [Lucas DeBiasio](#authors). In this project, we will be using Python to analyse if there is a correlation between provincial life satisfaction with sentiment in the corresponding provincial subreddit.

## Setup
Python libraries needed:
- `scipy.stats`
- `pandas`
- `matplotlib`
- `seaborn`
- `nltk`, library that contains the Vader sentiment analysis model 
    
Use this command to install the library, if needed: 

        pip install <library-name>


## Folder Structure

    .
    ├── data
    ├── scripts
    ├── plots
    ├── report.pdf
    └── README.md

* The `data` folder contains data used in the analysis including, life satisfaction data, reddit data and median income data.

* The `scripts` folder contains scripts used to obtain and analyze the data.

* The `plots` folder contains all plots produce by the analysis scripts.

## How to run the program

All script used below can be found in `/scripts` directory and all plots/figures can be found in `/plots` directory

1) Getting and Cleaning the data
- Run the `satisfaction-clean.ipynb` notebook to clean the satisfaction data. This notebook takes the `satisfaction-data-raw.csv` file from the `data/satisfaction-data` directory and returns to the same directory a file named `satisfaction-data-clean.csv` which is used for analysis.
- Run the `income-clean.ipynb` notebook to clean the income data. This notebook takes the `income-raw.csv` file from the `data/income-data` directory and returns to the same directory a file named `income-clean.csv` which is used for analysis.
- Reddit data is gathered and filtered using `get-reddit-data-spark.py` spark Python script. This script needs to be run in SFU compute cluster, this data produced by this script is not available in this repository since it too big. Instead, we have provided a filtered and cleaned Reddit data available in `/data/reddit-data` directory.

2) Analysis
- Run the `satisfaction-categorical-analysis.ipynb` notebook to perform the initial analysis of the satisfaction data itself and check if there is a correlation between province and life satisfaction. It also outputs the plot `life-satisfaction-rating.png`.
- Run the `sentiment-analysis.ipynb` notebook to generate an annual average sentiment score per subreddit and generate `sentiment_score_violinplot.png` which contains the dsitribution of sentiment scores in each subreddit.
- Run the `satisfaction-sentiment.ipynb` notebook to perform linear regression on the provincial satisfaction data and the subreddit sentiment score data. This notebook takes in `sentiment_score.csv` and `satisfaction-data-clean.csv` and outputs the figure `sentiment_score_vs_satisfaction_score.png`.
- Run the `income_satisfaction_analysis.ipynb` notebook to perform linear regression on subreddit sentiment score data and median income data. This notebook takes in `sentiment_score.csv` and `income-clean.csv` and outputs the figure `sentiment_vs_income.png`.

## Authors

- [Jocelyn Tandrea](https://github.com/jt1400)
- [Lucas DeBiasio](https://github.com/LucasDeBiasio)
