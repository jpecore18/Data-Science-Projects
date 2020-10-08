
# (Capstone) Project 6: Determinining Popularity of Rising Pop Music Artists with Scraped Spotify Data and NLP Sentiment Analysis

## Problem Statement
Spotify uses its popularity parameter in order to rank songs, albums, and artists. This "popularity" metric is based on how often users stream songs from Spotify. But how does this popularity metric by song-streaming compare with other metrics for popularity? 

What about popularity based on aspects of the music itself: like danceability, energy, and acousticness? What about popularity based on the content of an artist's lyrics--the verbal connotations and vibe of the poetry? And what about popularity based on Twitter users' reviews of the same music/artist? How do each of these factors influence our ability to predict the popularity of an artist or song? 

Finally, when using Regression modeling, Classification modeling, and Natural Language Processing Classification to predict the popularity of a musical artist, how can we use both these Spotify and non-Spotify popularity metrics to recommend which rising pop artists to fund, advertise, and support?

## Executive Summary
Spotify Song Attributes
1. First (for Song Attributes), I scrape three different playlists off of Spotify full of "Pop Rising" songs and stars. I clean the data, removing NAN values and duplicates for the songs. Spotify has a built in popularity function based on number of streams, so I will compare those popularity of songs to those I will generate via regression model.
2. Second, I use a wide variety of Regression models to predict popularity of a song based on the song's metrics (like energy, danceability, acousticness, etc.) that spotify's audio analysis algorithm produces. Next, I use a wide variety of Classification models to predict whether a song is popular (metric above 70 popularity according to Spotify) or not (based on quality). 
3. Finally, I interpret the differences between the stream-based popularity metric and this song-attribute-based popularity metric, generating reasons for incongruities.

Genius Lyric Attributes
3. First (for Lyric Attributes), I use the shorter list of playlist songs (just ordered_playlist) from Spotify as a basis for which lyrics to scrape. I scrape the lyrics for each of these songs off of Genius' lyric library.
4. Second, I use sentiment analysis and NLP to perform EDA on the most common words/sentiments for each song.
5. Finally, I try to evaluate whether there is a correlation between most common words and song sentiment with its popularity. 

Lyric Clustering Processing (Stretch Goal)
6. First (for Lyrics), I use Word2Vec/Spacey to cluster the lyrics on certain words. 
7. Finally, I try to evaluate whether there is a correlation between most common words and artist sentiment with their tweet popularity (positive tweets).

## Conclusions
Since the average test value for Regression analysis by Song Attributes was only 30% accurate (even though we had around 233,000 songs for the dataset with a wide variety of different features), we can determine that it is very difficult to determine the quality of a song by purely audio statistics. However, since the average test value for Classification modeling by Song Attributes (<75 popularity as 0 and >=75 popularity as 1 in a binary matrix) was above 90% consistently, we can conclude that we can predict whether a song is popular or not using Classification modeling with Song Attributes. Additional sentiment analysis of the Lyrics of a subset of these songs (lyrics from around 630 songs) shows that lyrics can act as a highly correlated factor to the popularity of the song. 

## Project 6 Contents:

1. Webscraping Spotify and Genius
2. Exploratory Data Analysis: Song Attributes
3. Exploratory Data Analysis: Lyrics and Sentiment Analysis
4. Regression Modeling: Song Attributes
5. Classification Modeling: Song Attributes
6. Clustering Song Lyrics

## Works Sourced
- General Assembly Data Science Immersive 2020
- https://www.kaggle.com/zaheenhamidani/ultimate-spotify-tracks-db
- https://developer.spotify.com/dashboard/applications/d7eee18620f34508b15f78ee4b9cfec4
- https://spotipy.readthedocs.io/en/2.14.0/#features
- https://www.marketwatch.com/story/how-spotify-influences-what-songs-become-popular-or-not-2018-06-18
- https://towardsdatascience.com/analysis-of-top-50-spotify-songs-using-python-5a278dee980c
- https://medium.com/@RareLoot/extracting-spotify-data-on-your-favourite-artist-via-python-d58bc92a4330
- https://developer.spotify.com/documentation/web-api/reference/playlists/get-playlists-tracks/
- https://developer.spotify.com/documentation/web-api/quick-start/
- https://nycdatascience.com/blog/student-works/web-scraping/spotify-x-billboard/
- https://ashleygingeleski.com/2019/11/11/spotify-web-api-how-to-pull-and-clean-top-song-data-using-python/
- https://towardsdatascience.com/country-wise-visual-analysis-of-music-taste-using-spotify-api-seaborn-in-python-77f5b749b421
- http://docs.tweepy.org/en/latest/
- https://slideslive.com/38931524/hitpredict-using-spotify-data-to-predict-billboard-hits?ref=account-60259-latest
- http://millionsongdataset.com/
- https://slideslive.com/38931325/hit-song-prediction-data-biases-and-evaluation-desing?ref=account-60259-latest
- https://towardsdatascience.com/how-to-build-a-fast-most-similar-words-method-in-spacy-32ed104fe498
- https://spacy.io/