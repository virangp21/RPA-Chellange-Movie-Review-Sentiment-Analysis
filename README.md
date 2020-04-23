# RPA-Challenge-Movie-Review-Sentiment-Analysis
## Introduction

This is an unattended bot that solves the Movie Review challenge from RPA Challenges. Bot uses Microsoft's Text Analysis API to get the sentiment from movie reviews. This is an example of bot using Machine Learning API to get sentiment using NLP. 

http://rpachallenge.com/movieSearch

## Challenges and Resolution

- Bot first opens the web page and randomly selects three movies to get their reviews. Selectors needs to be created  dynamically for each movie reviews to iterate through them. Using UI Explorer helps with identifying how indexes for selectors are changed. 

- Once you extract the movie review text form  P tags for each movie, next step is to find out if this is a positive review or negative  one. UiPath offers Cognitive activities package. You will need to download this package using Package Manager to your project.

- You will need to sign up for  Microsoft's text analysis API so that you can get API and Key to use within your project. UiPath appends the rest of the path to API so you only needs to specify part of the path in ServiceUrl property for Microsoft Text Analysis API ( e.q. "https://westcentralus.api.cognitive.microsoft.com/text/analytics/v2.1/" ). In Analysis type property then you need to select Sentiment as an option.    

## Conclusion

Obviously, this is a first cut version and there is lot desired in the implementation. One drawback of using Microsoft's text analysis API is there is no way to fine tune the machine learning model it uses to do the sentiment analysis. This results in not so perfect result. Another alternative to this is to built your  own machine learning model in python and plug it in.  

## Important Note

Anyone cloning this repository will need to provide their own API Key in Microsoft Text Analysis activity.  

Added azure devops yaml
