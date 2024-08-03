
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

1) Getting and Cleaning the data
- Run the `satisfaction-clean.ipynb` notebook in the `/scripts` directory to clean the satisfaction data. This takes the `satisfaction-data-raw.csv` file from the `data/satisfaction-data` directory and returns to the same directory a file named `satisfaction-data-clean.csv` which is used for the analysis.
- Run the `income-clean.ipynb` notebook in the `/scripts` directory to clean the income data. This takes the `income-raw.csv` file from the `data/income-data` directory and returns to the same directory a file named `income-clean.csv` which is used for the analysis.
- Something about get-reddit-data

2) Analysis


## Authors

- [Jocelyn Tandrea](https://github.com/jt1400)
- [Lucas DeBiasio](https://github.com/LucasDeBiasio)
