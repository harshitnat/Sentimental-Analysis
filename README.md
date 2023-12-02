# Sentimental-Analysis

import tweepy
from textblob import Textblob

consumer_key =
consumer_key_secret =


access_token =
access_token_secret =

auth = tweepy.OAuthHandler(consumer_key,consumer_key_secret)

auth.set_access_token(access_token,access_token_secret)

api = tweepy.API(auth)



for tweet on public_tweets:
    print(tweet.text)
    analysis = textblob(tweet.text)
    print(analysis.sentiment)
    if(analysis.sentiment[0]>0):
        print('Positive')
    elif analysis.sentiment[0]<0:
        print('Negative')
    else:
        print('Neutral')
    
