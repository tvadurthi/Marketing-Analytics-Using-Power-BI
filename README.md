# Marketing-Analytics-Using-Power-BI

**Problem Definition:**

Going though individual reviews manually and classifying them as positive or negative to gain insights for improving businesses is a tedious task. By automating these tasks, focus and resources can be shifted to improving the profitability. By using sentiment analysis on hotel reviews, we classify reviews as either positive or negative. Through the classification of the reviews, the hotel can understand and improve their reputation by focusing on their flaws. They can also understand self and competitors' customer perception better. Through large scale analysis of reviews, the hotel can identify their most critical and appraising factors. By comparing the sentiment of the reviews with demographic factors such as age group, gender and nationality, the hotel can better understand their current positioning. Based on this they can gain insights to revise their marketing campaign to better position, and target customers, which can improve business.

**Dataset Used:**

We will be taking raw textual data where the dataset has both negative and positive reviews. The data in the dataset contains text reviews for hotels in Europe. The dataset is a tabular .csv file. It has 17 features and 515739 records. 

**Methods Used:**

We consider only 20% of the dataset due to computational constraints. text data of reviews is pre-processed by conversion to lowercase followed by tokenization, removing punctuations, stop words, numbers, empty tokens and words with one letter. Text is lemmatized to base form. Using nltk’s sentiment analysis, a negative, neutral and positive score is calculated for each review. An overall sentiment score (compound score) is calculated through these scores. Reviews are classified as negative or positive based on compound score. The data set is explored on python in the following ways:

●	By taking the normalised count of negative reviews, the percentage of negative reviews is calculated.

●	Through WordCloud and matplotlib, most occurring words along with sentiments, based on the colour are pictorially displayed. 

●	Using seaborn, positive and negative review distribution with respect to compound score is plotted. 

Through gensim’s vectorizer reviews are vectorized. Tf-idf values of words are calculated and added as columns to the review dataset. The dataset is split into train and test sets to train a random forest model for classifying a review as negative or positive. The main purpose of this model is to identify dataset features most important to predict review sentiment. The model’s performance is evaluated through TP vs FP and Precision vs Recall ROC curves to get suitable threshold values. By selecting specific columns, custom data frames are exported for further data exploration on power BI.:

●	The ratio between positive and negative reviews classified based on compound score is represented.

●	Average hotel score for the countries is calculated and plotted.

●	Continent reviewer distribution is visualized.

●	Review data is grouped geographically to identify reviewed hotel density across Europe.

●	A visual comparison of the words in the text data before and after pre-processing of review text are represented according to their occurrence in the reviews.
Through the interactive interface of power BI, the exploratory analysis can be tweaked to gain deeper insights in data, for example instead of representing the countries with the highest average hotel ratings across the entire dataset, it can be represented according to average hotel ratings according to different geographical regions.

**Results:**

Based on the observations made, the following results were inferred:

●	The text review data considered post pre-processing contained words mainly conveying sentiment to hotel reviews. Redundant words were significantly reduced.

●	Based on the compound score calculated, 4% of the reviews in the dataset were classified as negative.

●	The distribution of positive reviews is more spread out around the mean as compared to the negative reviews with respect to compound score.

●	The most important dataset features to predict review sentiment are compound score, positive score and negative score.

●	The country with the highest average hotel rating across the dataset is identified as Austria. 

●	Majority of the reviews are from the United Kingdom, rating Austrian hotels the highest on average, contributing to 2% of the total negative reviews and 46% of the positive reviews.

●	The least number of reviews per country is the Democratic Republic of Congo with only 1 review and rating for a hotel in the United Kingdom.

●	Excluding 0 ratings, the lowest average hotel score given by any country is Libya. It gave an average of 7.4 out of 10 to hotels in Spain. Meanwhile Tanzania and Mozambique gave an average score of 9.3 out of 10 to Spanish hotels. This is the highest average rating given by any country.
