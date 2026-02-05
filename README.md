# **Twitter Sentiment Analysis Group Project**
![Sentiment Analysis Results](images/sentiment-analysis.jpg)

## **Business Understanding**
### **Overview**
This project aims to build NLP models that can predict the sentiment of tweets for Apple and Google products as either positive, negative or neutral.

The NLP base model will be a binary classifier focusing on the positive and negative reviews and will expand into a multiclass classifier capturing neutral sentiment reviews.

This will aid the companies in collection of reviews for their products and build or improve said products from the reviews.
### **Business Problem and Stakeholders**
Marketing and Branding teams at technology companies such as Apple and Google rely heavily on public feedback to shape brand strategies. Social media platforms such as twitter provide a large source of customer feedback that is difficult to analyze manually due to the nature of tweets(text). The business problem for this project is the need for a system that can accurately classify the sentiment of tweets towards the products as positive, negative or neutral.  
By automatically identifying changes in public sentiments, marketing brands and teams can track brand perception and respond more quickly to customer feedback. The model will support data-driven branding decisions by transforming raw tweets into actionable sentiment insights.
### **Objectives**
- Build an accurate sentiment analysis model

- Classify tweets as positive, negative, or neutral

- Extract meaningful insights from social media data

- Support improved brand perception and customer satisfaction
## **Data Understanding**
The dataset being used is a set of tweets about Apple and Google products evaluated by some contributors. The crowd was asked if the tweet expressed positive, negative, or no emotion towards the brand and/or product. If some emotion was expressed they were also asked to say which brand or product was the target of that emotion.  
This dataset contains 9093 data rows of tweets. It contains the tweets, the product/company and the sentiments.
## **Data Cleaning and Preprocessing**
The dataset had 22 duplicated entries and 1 sentiment without a text attached to it which were dropped. The `product/company` column was dropped too because it had too many missing values. There were also 156 sentiments classified as uncertain dropped since they added a lot of noise to our modeling process. We cleaned the text by converting it to lovercase, removing URLs, mentions, hashtags, punctuations and numbers.  
For preprocessing, we've used: a `RegexpTokenizer` for tokenization, stopwords removal, lemmatization using `WordNetLemmatizer`.  
## **Exploratory Data Analysis**
A countplot for sentiment distribution![A countplot for sentiment distribution](images/sentiment distribution.png)

## **Modeling and Evaluation**
Multiclass sentiment classification was performed on Positive, Negative, and Neutral tweets. Models trained: Complement Naive Bayes, LinearSVC, and Random Forest using TF-IDF features and class weighting. Evaluation used Precision, Recall, F1-score, and Macro F1-score. LinearSVC achieved the best Macro F1-score, indicating the most balanced performance across all classes.

## **Conclusion**
The support vector machine model was the most effective for this dataset. It balances
performance across all sentiment classes.

## **Recommendations**
1. SVM is recommended as the primary sentiment classification model due to its balanced
performance across sentiment classes.
2. Adopt a hybrid modeling approach, combining Naive Bayes for risk screening and SVM for
accurate sentiment confirmation and reporting.
3. Align model choice with business objectives, prioritizing recall for risk monitoring and
balanced performance for overall sentiment analysis.

