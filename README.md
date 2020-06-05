# Twitter-Sentiment-Analysis-on-Flask-App
In this repo i created a twitter sentiment analysis on flask app (web base).

# Dependentias
```python
from flask import Flask,render_template, redirect, request
import numpy as np
import tweepy 
import pandas as pd
from textblob import TextBlob
from wordcloud import WordCloud
import re
```

# Disclaimer
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

    consumerKey = ""
    consumerSecret = ""
    accessToken = ""
    accessTokenSecret = ""
    
    authenticate = tweepy.OAuthHandler(consumerKey, consumerSecret)
    authenticate.set_access_token(accessToken, accessTokenSecret)
    api = tweepy.API(authenticate, wait_on_rate_limit = True)
   ```



## ScreenShot
![](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Flask-App/blob/master/images/3.png)
![](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Flask-App/blob/master/images/4.png)
![](https://github.com/yogeshnile/Twitter-Sentiment-Analysis-on-Flask-App/blob/master/images/5.png)


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Follow on a Social Media
- [LinkedIn](https://bit.ly/2Ky3ho6)
- [Instagram](https://bit.ly/3b9Qeo4)
- [Instagram](https://bit.ly/32SXHV0) Personal
- [Twitter](https://bit.ly/3dbLJLC)
