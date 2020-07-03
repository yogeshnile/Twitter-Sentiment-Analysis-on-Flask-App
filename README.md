# Twitter Sentiment Analysis on FlaskApp :notebook:
In this repo i created a twitter sentiment analysis on flask app (web base).

[![](https://camo.githubusercontent.com/2fb0723ef80f8d87a51218680e209c66f213edf8/68747470733a2f2f666f7274686562616467652e636f6d2f696d616765732f6261646765732f6d6164652d776974682d707974686f6e2e737667)](https://python.org)

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


## Bug / Feature Request :man_technologist:
If you find a bug (the website couldn't handle the query and / or gave undesired results), kindly open an issue [here](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Flask-App/issues/new) by including your search query and the expected result.

If you'd like to request a new function, feel free to do so by opening an issue [here](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Flask-App/issues/new). Please include sample queries and their corresponding results.


## Connect with me! 🌐
Known on internet as **Yogesh Nile**

[<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/linkedin.png" title="LinkedIn">](https://bit.ly/2Ky3ho6)  [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/github.png" title="Github">](https://bit.ly/2yoggit) [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/twitter.png" title="Twitter">](https://bit.ly/3dbLJLC) [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/telegram-app.png" title="Telegram"/>](https://t.me/yogeshnile) [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/instagram-new.png" title="Instagram">](https://bit.ly/3b9Qeo4)  [<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/instagram.png" title="Instagram Personal">](https://bit.ly/32SXHV0)

## Email Me :e-mail:

[<img target="_blank" src="https://img.icons8.com/bubbles/100/000000/secured-letter.png" title="Mail me">](mailto:yogeshnile.work4u@gmail.com)
