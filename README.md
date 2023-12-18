<a name="br1"></a> 
<p align="center">

# Stock Market Prediction using Sentiment Analysis of Tweets
</p>

## Introduction

Over the past few decades, there has been significant developments in Internet based applications, therefore having a substantial impact on the Stock Market, along across the Globe. The advanced usage of the Internet has broken down the traditional barriers of geographical location, enabling the investors to buy and sell their shares through access to stock market status and moments from anywhere across the globe. This is further indicated by the advent of groundbreaking technologies like Artificial Intelligence(AI), Machine Learning, Big Data Analytics etc. We want to employ one of the advanced technologies implied above, Sentiment Analysis. With the help of Sentiment analysis of Tweets, and application of Support Vector Machine(SVM-Regressor), Artificial neural network(ANN), and Linear regression we plan to predict Stock Prices.

## Motivation

The beginnings of Web 2.0 era brought about significant change in discourse of the Internet, with gaining prominence of Social Media Platforms like Facebook, Instagram(along with Threads), X(formerly known as Twitter). People have started to express lots of their opinions and thoughts over these platforms about any particular topic such as news, movies or any new ventures in the market. The Information available on social media can be easily mined by company analysts for getting feedback as well as potential changes in the policy by responding to the public sentiment.Sentiment Analysis is used to classify any text into Positive, Negative, and Neutral sentiment, using VADER Lexicon(In Our Project). During the 20th century, the main investment theory was the Efficient Market Hypothesis (EMH). This theory states that the market reflects all the available information and that investors act rationally. However, the financial crises and the bubbles have demonstrated that sentiments and irrationality play a significant role in financial decision making. The Nobel Prize Robert Shiller challenged the EMH in an article in 1982 by comparing the US economy performances and the stock market during the 1920s. Several other distinguished economists have proved the presence of behavioural biases in stock market fluctuations. A new theory called “The Behavioral Finance Theory” attempts to explain these irrational components. Today, the fact that there is a part of irrationality in the stock market fluctuations is widely accepted. In order to try to capture public sentiment, investors daily use confidence indexes, polls and surveys.
A Couple of other important factors which further relays the importance of Sentiment Analysis are -

**1) Risk Management:** Understanding Market Sentiment can help investors avoid significant losses in their portfolio, and help them make their strategy accordingly.

**2) Identification of Trends and Patterns:** Sentiment analysis can uncover patterns and trends in public opinion that may precede or coincide with stock price movements. By identifying these patterns, investors can potentially make more informed trading decisions.

**3) News Impact:** News and media play a significant role in shaping investor perceptions. Sentiment analysis can help gauge how positive or negative news articles are, providing a clearer understanding of the potential impact on stock prices.

**4) Provides Competitive Advantage:** Brings more Adaptability to the Dynamics of Market, and Promotes Algorithmic Trading.

## Methodology

1) Importing Data from the Kaggle Database, with regards to the Tweet, Date, Stock Name and Stock Date. We also import the data for fluctuation in Stock Prize, Opening and Closing along with Volume.
Link- https://www.kaggle.com/datasets/equinxx/stock-tweets-for-sentiment-analysis-and-prediction
![1](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/db65f44d-fb78-4297-9661-129fc7fba4e5)
![2](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/c6e81392-0f46-43b3-93dc-3af01c7750e5)

2) We conduct Sentiment analysis on the tweets using VADER, and create a column for the sentiment(positive, negative or neutral)

3) After merging the Tweet and Stock Datasets, we conduct pre-processing data, remove neutral tweets as they have no effect on stock valuation, and plot the date-time series for various stock companies. A Variable Counter is created that accounts for the number of Tweets(positive or negative) as a direct correlation with fluctuations in stock.

4) Support Vector Machines(SVM) - We use SVM-Regressor to predict stock valuation with respect to the sentiment score, tweet volume and previous closing prices

5) Linear Regression and Artificial Neural Network(ANN) - We repeat the same modelling process with Linear Regression and ANN for comparison.

## Data Analysis:

● For the Date-Time series, we plotted the number of tweets(separately for both positive and negative), to understand which days the number of such tweets were highest, which helps in understanding the valuations of various company stocks.
![3](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/892d5b88-1bcb-4ba9-ade4-0d7dac351cdf)

● We have 25 companies' stock data, for the maximum is Tesla(17,562 tweets). We conduct the analysis of Positive tweets with respect to Valuation, for Tesla, Negative Tweets and draw the correlation matrix for both of them. 

![4](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/81d70f5b-8444-453e-bf31-736463dbc47f)
![5](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/3eeec448-71a0-46b6-8f2e-eec6562e265f)
![6](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/043abbe7-8fd9-43dd-a066-3129e0d24c5a)
![7](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/5db5f634-e80f-4a41-9637-bb364da8f3fd)

By Graphical Analysis and reading the Correlation matrix, we can somewhat see that positive and negative tweets do have some impact on the valuation, with the positive tweets showing higher correlation to fluctuation in stock price. The Correlation matrix identifies such relationships between various variables.

● We do such analysis for the remaining companies like Taiwan SMC and Apple, where we do such plots for Positive Tweets and Negative Tweets with valuation, along with correlation with Price Gain and Valuation.

## Modelling:

We then tried multiple models starting from linear classifiers to ANN regression. It can be seen that predicting whether the price of a stock will increase can be done with higher accuracy, than predicting the actual stock price, which is also intuitive. We modelled the output on the basis of the average of Sentiment Analysis Score of that day, and the stock prices on previous 3 days.

ANN Regression:

R-squared score: 0.30369780179991734

Linear Regression:

R-squared score: 0.3102219349408901

Support Vector Regressor:

R-squared score: 0.2188904312595099


![8](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/e09e0196-3f27-4ec7-a824-36bd49bbb9a6)

![9](https://github.com/shreyash23/Stock-Market-Prediction-using-Sentiment-Analysis-of-Tweets/assets/101019517/e6f207ad-3937-40f8-8aa0-f792da621925)

We also calculated the accuracy of the SVM-Regressor model to calculate the general trend of the market going up or down by comparing the slopes of predicted and real stock prices. It was observed that although the model was unable to predict the actual stock price with reliability, it was able to predict the general trend of the model with an accuracy of **80.95%.**

## Conclusion:

Towards the Conclusion of this project, It has provided valuable insights into the dynamic relationship between Social Media opinions and Stock Market prices and fluctuations. Employing the advanced learning algorithms like NLP, NLTK and integrating it with machine learning algorithms, we have demonstrated a potential correlation of social media opinions, especially Tweets with stock market fluctuations as a quantifiable result to make informed predictions.

While the results may not be perfect, we got 2 valuable insights into the correlation of tweet sentiments to stock market movement :-

1) The correlation between closing stock prices and sentiment score obtained from VADER is not strong enough to train a ML model with high accuracy to predict the exact stock closing price

2) While the exact stock price cannot be modelled, ML models produced a reliable result in modelling the sentiment score, tweet volume, and closing stock price over a window of 3 days against the General trend of the market i.e. if the market is going up or down with an accuracy of 80.95%. This provides valuable insight to the relation between tweets and stock market trends.

The project lays the foundation for further research and development in the field. The intersection of technology, finance, and sentiment analysis opens up new possibilities for understanding market behaviour and making more informed investment decisions.

