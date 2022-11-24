<div align="center">

    <h1>Stock Market Prediction Using Sentiment Analysis on Twitter(In progress)</h1>
    
    <p>Apply Sentiment Analysis on forum corpus data, and used it for stock market trend prediction.

    There is two parts of this project: English and Chinese.</p>
    
</div>

<!-- Badges -->
<p>
  <a href="">
    <img src="https://img.shields.io/github/contributors/Louis3797/awesome-readme-template" alt="contributors" />
  </a>
  <a href="">
    <img src="https://img.shields.io/github/last-commit/Louis3797/awesome-readme-template" alt="last update" />
  </a>
</p>

## English derivative

Applied **Opinion Finder**, **GPOMS** and **bi-LSTM** on large-scale Twitter feed to conduct sentiment analysis, model achieved 75% accuracy and 0.9% MAPE in stock market index trend forecasting.

**Google-Profile Of Mood States (GPOMS)** is an extended version of POMS-bi. It is based on a lexicon of 964 terms and can measure human mood states in six mood dimensions : Calm, Alert, Sure, Vital,
Kind and Happy, it scaled from -1 to 1 for each dimensions.

**Opinion Finder** is a tool for sentiment analysis using 4 emotional lexicons.

### Step 1: Data Preprocessing

> 1_Data_preprocessing_NewData.ipynb

Conducting data pre-processing onto twitter feeds.

### Step 2: Sentiment Analysis 

> 2_GPOMS_SA.ipynb / 2_Opinion_Finder_SA.ipynb

Sentiment analysis using **GPOMS** and **Opinion Finder**.

### Step 3: Granger Causality Analysis

> 3_Granger_Causality.ipynb

Using **Granger Causality** to detect whether there is correlation in time series.

### Step 4: Build Time Series Forecast Model

> 4_GPOMS_LSTM.ipynb / 4_OF_LSTM.ipynb

Using **bi-LSTM** to build a time series model and estimate the confidence interval for the accuracy.

### Step 5: Portfolio Management

> 5_Portfolio_Management.ipynb

Build portfolios and calculate its performance.

### Step 6: Related graph

> 6_Plotting.ipynb

Result preview

## Chinese derivative

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