# Evaluating New Marketing Campaign Performance (A/B Testing)
- [Introduction](#introduction)
- [How to Use](#how-to-use)
- [Methods](#methods)
- [Results ](#results)

## Introduction
This project aims determine if a new marketing email design results in more traffic being directed towards a website's landing page. The goal is to design an experiment to test this hypothesis, and then to analyze the findings for a statisticially significant difference between the conversion rates of the old and new email designs. Significance tests such as the Z-test and confidence intervals are used to determine if our results are statistically significant.

## How to Use

### For Direct Replication of Results
1. Download the [email_testing.ipynb](email_testing.ipynb) file.
2. Download the "ab_test_data.csv" file.
3. Ensure that the .ipynb file and the .csv file are in the same folder, or that you have made the necessary changes to the file path in the code.
4. Ensure you have the libraries numpy, pandas, scripy, statsmodels, matplotlib, and seaborn installed on your machine.
6. Run the notebook!

### For Running Your Own Experiment
1. Download the .ipynb file.
2. Download the "ab_testing_data.ipynb"

## Methods
The data were first loaded and preprocessed, ensuring proper data types and indexing. Then preliminary visualizations were created. Next, time series analysis using rolling mean and standard deviation was conducted. 

![Nuclear Production Rolling](images/nuclear%20rolling%20mean.png)

This was followed by ADF and autocorrelation testing as well as trend decomposition. Then, the data were split into train and test sets and time series forecasting was done using ARIMA. 

![Nuclear Production TestTrain](images/nuclear%20train%20test.png)

The ARIMA model was finally evaluated using RMSE.

## Results

The U.S.'s nuclear electric energy production was shown to have increased greatly from 1973 to about 2000, when it then leveled off and remained stable up until the present day. 

![Nuclear Production Line Plot](images/nuclear%20line%20plot.png)

The data was shown to be stationary, autocorrelated, and non-seasonal. 

![Nuclear Production Trend Decomp](images/nuclear%20trend%20decomposition.png)

The ARIMA(3,1,5)(0,0,0)[0] model was able to effectively forecast nuclear energy production with a low RMSE of 0.04, indicating good prediction accuracy. 

![Nuclear Production TestTrainPred](images/nuclear%20train%20test%20pred.png)
