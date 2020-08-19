# Twitter Sentiment Analysis on FlaskApp :notebook:
In this repo i created a twitter sentiment analysis on flask app (web base).

[![](https://camo.githubusercontent.com/2fb0723ef80f8d87a51218680e209c66f213edf8/68747470733a2f2f666f7274686562616467652e636f6d2f696d616765732f6261646765732f6d6164652d776974682d707974686f6e2e737667)](https://python.org)

You can also check a demo website :point_right: [click here](http://hitalfashion.pythonanywhere.com/)
# Directory Tree :cactus:
```bash
.
├── images
│   ├── 1.png
│   ├── 2.png
│   ├── 3.png
│   ├── 4.png
│   └── 5.png
├── LICENSE
├── main.py
├── README.md
├── static
│   ├── logo.png
│   └── style.css
└── templates
    ├── index.html
    └── sentiment.html

3 directories, 12 files
```

# Technology used in Project :hotsprings:
<img target="_blank" src="https://github.com/yogeshnile/technology/blob/master/Flask.png" width="300">     <img target="_blank" src="https://github.com/yogeshnile/technology/blob/master/pandas.png" width="300">    <img target="_blank" src="https://github.com/yogeshnile/technology/blob/master/numpy.png" width="200">      <img target="_blank" src="https://github.com/yogeshnile/technology/blob/master/tweepy.webp" width="200">     <img target="_blank" src="https://github.com/yogeshnile/technology/blob/master/textblob.png" width="200">    <img target="_blank" src="https://github.com/yogeshnile/technology/blob/master/wordcloud.png" width="300">

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

[![][I_LinkedIn]][LinkedIn]  [![][I_Github]][Github] [![][I_Twitter]][Twitter] [![][I_Telegram]][Telegram] [![][I_Instagram]][Instagram]  [![][I_Instagram Personal]][Instagram Personal]   [![][I_discord]][discord]

## Email Me :e-mail:

[![][I_Email]][E-mail]

[LinkedIn]: https://bit.ly/2Ky3ho6
[Github]: https://bit.ly/2yoggit
[Twitter]: https://bit.ly/3dbLJLC
[Telegram]: https://t.me/yogeshnile
[Instagram]: https://bit.ly/3b9Qeo4
[Instagram Personal]: https://bit.ly/32SXHV0
[E-mail]: mailto:yogeshnile.work4u@gmail.com
[discord]: https://discord.gg/R2ug3gR

[I_discord]: https://img.icons8.com/bubbles/100/000000/discord-logo.png
[I_LinkedIn]: https://img.icons8.com/bubbles/100/000000/linkedin.png
[I_Github]: https://img.icons8.com/bubbles/100/000000/github.png
[I_Twitter]: https://img.icons8.com/bubbles/100/000000/twitter.png
[I_Telegram]: https://img.icons8.com/bubbles/100/000000/telegram-app.png
[I_Instagram]: https://img.icons8.com/bubbles/100/000000/instagram-new.png
[I_Instagram Personal]: https://img.icons8.com/bubbles/100/000000/instagram.png
[I_Email]: https://img.icons8.com/bubbles/100/000000/secured-letter.png
