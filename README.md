## Do tweets on Bitcoin predict the price of Bitcoin?


## Table of contents
- [Background](https://github.com/Jenniferdersjant/Final_project/blob/main/README.md#background)
- [Methodology](https://github.com//Jenniferdersjant/Final_project/blob/main/README.md#methodology)
- [Data](https://github.com//Jenniferdersjant/Final_project/blob/main/README.md#data)
- [Key findings](https://github.com/Jenniferdersjant/Final_project/blob/main/README.md#key-findings)
- [Conclusion](https://github.com//Jenniferdersjant/Final_project/blob/main/README.md#Conclusion)
- [Reflection](https://github.com//Jenniferdersjant/Final_project/blob/main/README.md#Reflection)


## Background
It seems as if everytime Elon Musk tweets something about the Bitcoin, the Bitcoin price seems to adjust accordingly. Is there really a correlation between the tweets about Bitcoin and the Bitcoin prices? Read more of this research to find out. 


<p align="center">
  <img src="https://cdn.vox-cdn.com/thumbor/kRoX7XGXHMCqTtvu4KGGeoqmBdI=/0x0:5021x3161/920x613/filters:focal(2110x1180:2912x1982):format(webp)/cdn.vox-cdn.com/uploads/chorus_image/image/69306217/1232949232.0.jpg" />
</p>


## Methodology
In order to research this question, Twitter's API has been used to scrape tweets with the text query Bitcoin in them. Since the API from Twitter is very limited in use, a sleep timer is used to scrape as much as possible. Historic Bitcoin price data could be found on multiple sources. To get the most data as possible, Bitcoin prices per minutes were used. Based on a regression between the number of tweets on Bitcoin and Bitcoin price, you can not really say something about causality. That is why a sentiment analysis is done to get the polarity of the tweets. 

These three dataframes are subsequently clean, grouped per day, hour and minute and combined in order to do correlations and machine learning.

## Data
Based on the limited amount of data that could be scraped in the API from Twitter, 1000 tweets have been scraped, which accumalates to roughly 19 tweets per second which contain the word Bitcoin. When this is grouped per minute, a dataframe with 56 rows is established. Sentiment is calculated based on a group by as well, with taking the average polarity per minute. Bitcoin data per minute is found on Gemini data.

## Key findings
When looking at several regressions, it is clear that they descriptive variables sentiment and tweet count are not highly correlated with the Bitcoin price, with a score of 0.23 and 0.36 respectively. A F-test has been done as well to look for the combined effect of the descriptive variables on the Bitcoin price. This gives an even lower result of 0.21 correlation. 
Machine learning has been done as well to check for the predictive power of tweet count and sentiment on the Bitcoin price. A train test split has been performed where 70% of the data is used for testing the model. The output gives a R2 score of   XX and a absolute mean error of 58.6 USD, meaning that the predictive power is of by almost 60 USD per minute.

## Conclusion
Predicting the Bitcoin price has been something that several brokers, financial institutions and researchers have struggled with. It has one of the highest volatility prices, which can sometime be hard to explain. Unfortunately, the amount of tweets on the bitcoin is not a very good descriptive variable for the Bitcoin and therefore not a valid predictor as well.

## Reflection
It has to be noted that there are several limitation to this research. The first one is the limited amount of data that could be obtained from Twitter. Gathering more data could increase the descriptive and predictive power of this variable. Furthermore, this research has not taken into consideration time lags. It could be the case that a lag of the tweets 5 minutes, 15 minutes or even an hour could have some effect on the prices of Bitcoin. Lastly, there are other descriptive variables that explain the volatile price of the Bitcoin, for further research those variables should be added as well.
