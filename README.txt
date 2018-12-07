Goal:
Python Library:
from bs4 import BeautifulSoup
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import datetime
from datetime import datetime
from pandas_datareader import data as web
import os
import string
import requests
import nltk
from nltk import word_tokenize
from nltk.corpus import PlaintextCorpusReader
from nltk.corpus import stopwords
from nltk.tokenize import TweetTokenizer
from nltk.tokenize import word_tokenize
from nltk.stem import PorterStemmer
from nltk.stem import WordNetLemmatizer
import re
from textblob import TextBlob
import sklearn
from sklearn.feature_extraction.text import TfidfVectorizer, CountVectorizer
from xgboost import XGBClassifier
from sklearn.metrics import accuracy_score

Procedure:
First: Web Scraping Data
1. Scraping stock price from yahoo finance by using BeautifulSoup, get S&p500 Index from Sept.26 2016 to Oct.1 2018.
2. Scraping news title and news abstract from Wall Street Journal(http://www.wsj.com) by using BeautifulSoup.
3. Convert Scraping results into DataFrame using pandas, and write out .csv file as our project data.
4. Output File are news.csv and Stock_Price.csv

Second: Data virtualization
1. ...


Third: News data Textmining
1. Filter Text by using NLTK  and many inner-packages:
Remove digits, remove white space, remove stopwords, lemmatizer. Then write into .csv as "newscleaned1.csv"
2. Using sklearn package to count words frequency on both title and abstract, delete the low frequency words(<5) 
and re-orgnize text data file into data frame. Then wrote out .csv file as "newscleaned2.csv"

Fourth: Stock Price Preprocessing
... Then our response varibale Y formed.

Fifth: Text segmentation and Polarity Analysis
1. Using Textblob to do this step. Convert both news title and news abstract to two-dimensional columns
polarity and subjective. Then our explantory varible X formed. 
2. Other polarity Methods

Sixth: Partition Training and Test
1. Using the first 70% data as train, and last 30% data as test. Using this partition on both X and Y.
2. Other cutting methods

Seventh: Modelling
1. USing XGBoost to train our model. After tuning, eventaully get test accuracy: 0.8507042253521127.

Eighth: Result analysis
1. ...




