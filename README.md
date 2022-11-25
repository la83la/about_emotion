# Stock Market Prediction Using Sentiment Analysis on Twitter (In progress)
    
### Apply Sentiment Analysis on forum corpus data, and used it for stock market trend prediction.

There is two parts in this project: English and Chinese.
    

<!-- Badges -->
<p>
  <a href="">
    <img src="https://img.shields.io/badge/contributors-2-yellow" alt="contributors" />
  </a>
  <a href="">
    <img src="https://img.shields.io/badge/last%20update-November%202022-green" alt="last update" />
  </a>
</p>

## English derivative

Applied **Opinion Finder**, **GPOMS** and **bi-LSTM** on large-scale Twitter feed to conduct sentiment analysis, and used it for market index trend forecasting.

**Google-Profile Of Mood States (GPOMS)** is an extended version of POMS-bi. It is based on a lexicon of 964 terms and can measure human mood states in six mood dimensions : Calm, Alert, Sure, Vital,
Kind and Happy, it scaled from -1 to 1 for each dimensions.

**Opinion Finder** is a tool for sentiment analysis using 4 categories of sentiment lexicon.

### Step 1: Data Preprocessing

> 1_Data_preprocessing_NewData.ipynb

Conducting data pre-processing onto twitter feeds.

Size of tweets | Time Duration 
--- | --- 
923,673 | 2020/04/09 ~ 2020/07/16 (77 days)

![alt text](https://github.com/la83la/about_emotion/blob/main/English_derivative/tweets_size.png "Tweet size")

Tweet size

### Step 2: Sentiment Analysis 

> 2_GPOMS_SA.ipynb / 2_Opinion_Finder_SA.ipynb

Sentiment analysis using GPOMS and Opinion Finder.

Analysis result: **Alert** is the highest estimator in GPOMS analysis.

### Step 3: Granger Causality Analysis

> 3_Granger_Causality.ipynb

Using **Granger Causality** to detect whether there is correlation in time series.

Granger Causality test is used to determine whether or not one time series is useful for forecasting another. This test uses the following null and alternative hypotheses:

* Null Hypothesis (H0): Time series x does not Granger-cause time series y
* Alternative Hypothesis (HA): Time series x Granger-causes time series y

If the p-value is less than a certain significance level (i.e. α = .05), then we can reject the null hypothesis and conclude that we have sufficient evidence to say that time series x Granger-causes time series y. In this chapter, we use the processed sentiment values as x-column, to calculate its relationship with the stock prices(as y-column).

Sentiment with causality (p-value < 0.05):

1. Sure
2. Alert


### Step 4: Build Time Series Forecast Model

> 4_GPOMS_LSTM.ipynb / 4_OF_LSTM.ipynb

Using **bi-LSTM** to build a time series model and estimate the confidence interval for the accuracy.

 | Opinion Finder | GPOMS-Alert | GPOMS-Sure | GPOMS-Alert+Sure | GPOMS-Alert+Vital
--- | --- | ---
MAPE | 1.57% | 1.7% | **0.9%** | 1.75% | 1.59%
Directional accuracy | 65% | 64% | **75%** |  60% | 56 %

![alt text](https://github.com/la83la/about_emotion/blob/main/English_derivative/model%20result.png "Model result")

Model result

### Step 5: Portfolio Management

> 5_Portfolio_Management.ipynb

Build portfolios and calculate its performance.

### Step 6: Related graph

> 6_Plotting.ipynb

Project Related Charts

## Chinese derivative (In progress)

### Crawler
Chinese news and cover image crawler.
> News_crawler.ipynb / Picture_crawler.ipynb

### Preprocessing

Emoji Processing:
> Frequency_word_classification.ipynb

text Processing: 
> preprocess(C).ipynb

### Word Frequency

Calculate word frequency
> NewsWordFrquency.ipynb / Frequency_word_classification.ipynb