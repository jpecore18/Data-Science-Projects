# Coding Projects Overview (Most Current by Reverse Chronological Order)
- Project 6 (Capstone): Deteminining Popularity of Rising Pop Music Artists with Scraped Spotify Data and NLP Sentiment Analysis
- Project 5: Estimating Flood Depths of Submerged Vehicles with Convolutional Neural Networks (cNN)
- Project 4: Predicting Income Bracket of Citizens with their Demographic Backgrounds
- Project 3: Predicting Dating App Subreddit with Natural Language Processing
- Project 2: Predicting House Sale Prices with Machine Learning
- Project 1: SAT & ACT Analysis

# Project 6 (Capstone): Deteminining Popularity of Rising Pop Music Artists with Scraped Spotify Data and NLP Sentiment Analysis

## Problem Statement
1. Spotify uses its popularity parameter in order to rank songs, albums, and artists. This "popularity" metric is based on how often users stream songs from Spotify. 

2. But how does this stream-popularity metric compare with other metrics for popularity? 
    - This metric only shows how popular very recent artists are in general (not popularity according to genre or popularity by song/lyrical content). 

3. As a result, historically VERY popular classic songs (by Earth, Wind, & Fire, The Beatles, and other "classic groups") are overlooked. Additionally, artists who are VERY popular in their genre become ignored due to higher weight artists from higher popularity genres like "pop." 

4. We need a new metric for popularity. In fact, we need more than one new popularity metric and a logic to guide our new metrics for popularity, in addition to a way of evaluating our old metric's effectiveness.

So:

1. Can we predict a song's popularity by stream count accurately using Regression Modeling?

2. Can we predict whether a song is popular by stream count using Classification Modeling?

3. What can we say about a song's popularity based on aspects of the music itself: like danceability, energy, and acousticness? 

4. What can we say about a song’s popularity based on the content of an artist's lyrics--the verbal connotations and vibe of the poetry? 

5. How do each of these factors influence our ability to predict the popularity of an artist or song?

6. Finally, when using Regression modeling, Classification modeling, and NLP Clustering to predict the popularity of a musical artist, how can evaluate whether or not to trust Spotify's ranking of popularity? 

7. What other metrics of popularity should we define and recommend that Spotify and other top streaming sites adopt? What is our reasoning?

## Executive Summary
Spotify Song Attributes
1. First (for Song Attributes), I scrape ten different playlists off of Spotify full of 700 "Rising" songs from 2020. I clean the data, removing NAN values and duplicates for the songs. Spotify has a built in popularity function based on number of streams. This is ordered_playlist. Then, I import a dataframe of 232,000 songs from 2018-2020 made by a prominent Kaggle musical data scientist, Zaheen Hamidani, to the small dataset. I clean this data, dropping NAN values and duplicates. Next, I concatenate this songlist to ordered_songlist. At last, I name this large dataframe of roughly 150,000 songs as giant_ordered_playlist.
2. Second, I build a wide variety of Regression Models that try to accurately predict a song's "stream-popularity" based off of the song's musical attributes (like energy, valence, modality, time signature, and other characteristics). I will also use many different Classification Models to measure whether we can predict that a song is popular (above 75% popularity on a scale of 0 to 100) based off of these same song attributes. 
3. Finally, I interpret the differences between the stream-based popularity metric and this song-attribute-based popularity metric, generating reasons for incongruities and making conclusions about the effectiveness of our popularity metric.

Genius Lyric Attributes
3. First (for Lyric Attributes), I use the shorter list of playlist songs (just 700 songs from ordered_playlist) from Spotify as a basis for which lyrics to scrape. I scrape the lyrics for each of these songs off of Genius' lyric library.
4. Second, I use sentiment analysis and NLP (CountVectorizer) to perform EDA on the most common words/sentiments for each song.
5. Finally, I try to evaluate whether there is a correlation between most common words and song sentiment with its popularity. 

Lyric Clustering Processing (Completed Stretch Goal)
6. First (for Lyrics), I use Spacey to convert the lyrics of the 300 most common words in each song of ordered_playlist into vectors. These word vectors are arranged by their similarity to one another on a large coordinate plane. 
7. Finally, I try to evaluate whether there is a correlation between a group of lyrics' content and their artist's stream-popularity. I conclude that yes, there IS a clear relationship between a song's stream-popularity and lyrical content. Though, for further research, I would like to pursue Hypothesis Testing to be certain of this relationship being a correlation at a statistically significant level.

# Project 5: Estimating Flood Depths of Submerged Vehicles with Convolutional Neural Networks (cNN)

### Problem Statement

Both a car insurance company and a motor-vehicle owner have a vested commercial interest in being able to estimate a car's damages caused by natural disasters, floods in particular. The United States 2020 Census recognizes floods as the most common natural disaster in the country, and cars are particularly vulnerable to flood damages due to their internal technologies. The 2019 Mississippi River Floods resulted in 20 Billion Dollars of damages alone. 

As a result of these factors, we need to be able to use Visual APIs, Machine Learning, and Neural Networks to systematically label the depths of flooded motor vehicles. Which APIs and forms of Machine Learning will we use to recognize our target variable "flood depth?" More importantly, how accurately can we estimate flood depth, considering the baseline flood depth predictions are only 20% accurate for this type of model.

### Executive Summary
- After extensive research, we decided to use the Google Vision API to specifically identify flooded from non-flooded cars. 
- We created a dataset of flooded and non-flooded cars from public domain image sources. 
- Next, we used Google Vision’s API to label specific objects like “wheel,” “window,” etc. in our dataset.
- Then, we trained the Google Vision API to recognize flooded cars as different objects from non-flooded cars.
- To enlarge our dataset, we used Image Augmentation to visually bootstrap our images. 
- We assigned Flood Height to these images.
- Finally, we inputted our processed flooded vehicles through our Convolutional Neural Network, successfully estimating flood height with visual images.

# Project 4: Predicting Income Bracket of Citizens with their Demographic Backgrounds

### Problem Statement
In this project we seek to identify individuals who have an income above 50,000 dollars per year using information about their education, family, age, occupation and nationality. We will use a limited dataset to train classification models and determine the best predictors and models.

### Executive Summary
Data was cleaned and dummified. Native country data was binarized to 1 for US native and 0 for otherwise. Engineered features were tested but none were used in the final models. Models fit were Decision Tree, Random Forest, Extra Trees, Logistic Regression, K-Nearest Neighbors, SVC, GradientBoost, and AdaBoost. All models were tested with bagging classifiers for bootstrapping after optimizing individually on non-bootstrapped train/test splits. Bootstrapping was weighted using the 'fnlwgt' column of the data in order to get a sample that is better representative of the population.

# Project 3: Predicting Dating App Subreddit with Natural Language Processing

### Problem Statement
As a representative of the Match company, providing good customer service is essential to the wellbeing of our dating platform Tinder. As a result, we want to know how similar Tinder and Tinder Stories are as subreddits. Can a logistic regression and other classification form of models accurately predict (< 60-80 % of the time) the difference between a reddit post on Tinder Stories and one on Tinder? Moreover, what is the most frequent verbal content that Tinder produces on a huge, statistical level? What differentiates the users and contents of Tinder's subreddit from Tinder Stories' subreddit. Finally, what can I recommend for the board of Tinder to do in order to investigate and re-evaluate the reputation of Tinder set by its community of users?

### Executive Summary
By using Natural Language Processing techniques such as Count Vectorizer and four different kinds of classification models, I found out something interesting; heterosexual men would tend to use the Tinder Subreddit to talk about dating women, while heterosexual women would tend to use the Tinder Stories Subreddit to talk about dating men. We can gather this because "removed," "girl," and "girls" are three of the top most popular words in "Tinder" as a subreddit. Likewise, "guy" and "date" are two of the most popular words in "Tinder Stories'" subreddit. 

As most of the Tinder Subreddit posts contain images and most of the Tinder Stories Subreddit posts contain words-indicating that in this environment, these men are more visual and these women are more verbal. The models used can accurately predict the differences between posts on each of these subreddits between 87% and 97% of the time, indicating that gendered words and preferences such as these impact our models rather significantly. These gendered words can be used to inform how we build our User Interface more effectively for each group.

# Project 2: Predicting House Sale Prices with Machine Learning

### Problem Statement
The AMES Housing Data Set represents the amenities of over 2900 properties in Ames, Iowa priced and sold from 2006 to 2010. Over 75 distinct variables divide these amenities into categories. 

The four categories of amenities for each house are categorical, ordinal, discrete, and continuous. Categorical (or nominative) values, such as neighborhood or type of roofing, lack a hierarchy of quality and possess qualitative information. Ordinal values possess a clear hierarchy (like Kitchen Quality (Excellent, Good, Average, Poor)) but still represent qualitative information. Discrete variables are countable (like Number of Cars) and quantitative. Finally, continuous variables are quantitative, measurable, and can contain fractions of values (like Square Footage). 

How can this information be used by Real Estate developers and clients to predict or increase a property's value? Moreover, how can a data scientist use a model to process all of this data?

### Executive Summary
By using the form of Machine Learning called Linear Regression, this project processes through a database of AMES Housing training data. Then, linear regression predicts a house's sale price and value using the training data's trends and properties. Additionally, regression techniques (such as feature engineering and selection) enhance the quality of our predictions.

### Conclusions

One can use linear regression to greatly reduce errors and improve the performance of predicting sale price based on a variety of highly correlated factors. Although, it seems that knowing which factors influence a house's price (such as Kitchen Quality and Bathroom Space) can often be more valuable than the predictive model itself. As a result, even the basic method of Linear Regression can be incredibly useful for a firm's Real Estate pricing decisions.

The interpretability of linear regression (as opposed to more complex models) makes it one of the more easy models to make inferences with. We have the ability to note which features correlate with Sale Price to be able to improve the price. Additionally, we also have the relative correlations of Sale Price with other factors, giving us an actual quantitative idea of how to advise a Real Estate branch on how to recreate their properties.

# Project 1: SAT & ACT Analysis

### Problem Statement
Geographically, the United States remains divided by more than just geology. For each state, the participation rate of their high school students in the SAT vs ACT varies wildly. Yet, clear trends and correlations emerge. Why do some states remain loyal to only one test? Moreover, which specific factors influence the popularity of tests? Additionally, how do political and economic factors influence the layout of the test landscape? Finally, what can we suggest to raise participation rates.

### Executive Summary
The ACT dominates the SAT rate all three years in terms of participation. This results from State-Required Testing, Self-Selection, Economic Inequality, and Political Bias. To increase participation, we recommend that the SAT Board streamline the Fee Waiver Application Process, get rid of SAT Subject Tests, increase State-Required SAT Tests, add Science as its own Subject, and politically insist on the importance of SAT testing.