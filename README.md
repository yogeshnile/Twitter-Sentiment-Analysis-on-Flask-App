# Twitter-Sentiment-Analysis-on-Flask-App :notebook:
In this repo i created a twitter sentiment analysis on flask app (web base).

You can also check a demo website [click here](http://hitalfashion.pythonanywhere.com/)

# Dependentias :warning:
```python
from flask import Flask,render_template, redirect, request
import numpy as np
import tweepy 
import pandas as pd
from textblob import TextBlob
from wordcloud import WordCloud
import re
```
# Application :loudspeaker:
Ckeck out Twitter Sentiment Analysis on python **GUI** App :point_right: [click here](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Python-GUI)

Ckeck out Twitter Sentiment Analysis on python **Jupyter Notebook** :point_right: [click here](https://github.com/yogeshnile/Sentiment-Analysis-of-Twitter-Account)

# Disclaimer :skull_and_crossbones:
I am not provideing twitter **API** keys. You have get twitter API keys on twitter developer account. Get [API Keys](https://developer.twitter.com/)

Get a API key and put in the below code section
```python
def sentiment():
    userid = request.form.get('userid')
    hashtag = request.form.get('hashtag')

    if userid == "" and hashtag == "":
        error = "Please Enter any one value"
        return render_template('index.html', error=error)
    
    if not userid == "" and not hashtag == "":
        error = "Both entry not allowed"
        return render_template('index.html', error=error)
    
    #=====================Insert Twitter API Here==========================
    consumerKey = ""
    consumerSecret = ""
    accessToken = ""
    accessTokenSecret = ""
    #=====================Insert Twitter API End===========================
    
    authenticate = tweepy.OAuthHandler(consumerKey, consumerSecret)
    authenticate.set_access_token(accessToken, accessTokenSecret)
    api = tweepy.API(authenticate, wait_on_rate_limit = True)
   ```



## ScreenShot :camera_flash:
![](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Flask-App/blob/master/images/3.png)
![](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Flask-App/blob/master/images/4.png)
![](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Flask-App/blob/master/images/5.png)


## Contributing :man_technologist:
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Follow on a Social Media :busts_in_silhouette:
- [LinkedIn](https://bit.ly/2Ky3ho6)
- [Instagram](https://bit.ly/3b9Qeo4)
- [Instagram](https://bit.ly/32SXHV0) Personal
- [Twitter](https://bit.ly/3dbLJLC)
