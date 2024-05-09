# KET NLP Analysis for Apple product
## Introduction
In todays digital world social media plays a vital role in collecting data .Twitter is one of the social media which  has a huge sources of consumers opinion and sentiments. Analyzing these data using Natural Language Processing(NLP) techniques offer valuable insight in to public perceptions of brands and products.This introduction outlines the process of conductingNLP analysis for apple product sentiment on Twitter.

KET the Apple Marketing team wants to review negative sentiments expressed on Twitter about Apple products during the SXSW conference.

![image](https://github.com/ermiyas-sidama/NLP-Analysis-for-Apple-product/assets/160514617/1e98365a-023e-4ebe-94c2-1d3ecf62c47b)

Photo by ([Clément Delteil](https://pub.towardsai.net/unsupervised-sentiment-analysis-with-real-world-data-500-000-tweets-on-elon-musk-3f0653135558))


## Project Overview

This project tries to investigate and analyze negative sentiment sourrounding Apple products as expressed during the 2013 South by SouthWest(SXSW) Conference using Natural language Processing techniques.Understanding negative sentiment is very important for companies like Apple to refine product strategies and enhance customer satisfaction.So this analysis aims to find insights crucial for product  refinment and strategic decision making.
## Business Problem

KET the Apple Marketing team wants to review negative sentiments expressed on Twitter about Apple products during the SXSW conference.
1. What aspects of Apple products do users frequently critique?
2. What is a common point of frustration for consumers regarding the performance of Apple devices?
3. What specific concerns do users raise regarding aesthetics and user interface?

## Data and Resource Used

The dataset utilized in this project originates from CrowdFlower (Data.World), where human raters assessed sentiment in over 9,000 tweets, categorizing them as positive, negative, or neutral. Our focus was on the positive and negative sentiment categories, which encompass approximately 3,000 records.

![image](https://github.com/ermiyas-sidama/NLP-Analysis-for-Apple-product/assets/160514617/8aa2b1f5-0bf3-4f83-8ff1-725745d7f3fa)



The depicted figure illustrates a class imbalance within the dataset. To address this, we employed a strategy of augmenting our dataset by incorporating additional negative tweets. This approach aims to provide the model with a more balanced representation of negative sentiments, thereby enhancing its ability to accurately classify negative tweets.
Key aspects of this project include:
- Utilization of Python 3, leveraging the Natural Language Toolkit (nltk) package among others, for text data preprocessing.
- Integration of Tableau for data visualization purposes.
  
## Data Preprocessing

- Cleanse and preprocess the text data to enhance its quality and consistency for analysis.This involved steps such as tokenization,removing stop words and punctuation and lemmatization text data.
- WordClound visualization with Negative sentiment on Apple product was generated to provide an intuitive representation of frequently occuring words or phrase associated with negative sentiment.
- Associate negative sentiment with specific Apple products, features, or aspects to pinpoint areas of concern.

## Modeling

Leveraging machine learning models for sentiment analysis of tweets about Apple enables the company to gain valuable insights into customer perceptions, preferences, and opinions, facilitating informed decision-making and enhancing the overall customer experience. We now want to run a Binary Classification model that will be trying to correctly predict whether a tweet is "Positive" or "Negative.
As a starting point, the team created a simple MultinomialNB model as a baseline model based on our domain knowledge. Then, the team created 5 additional models to improve classification performance by tuning the hyperparameters and also tries to see the addition of extra negative sentiment Tweet on apple product. The team chose accuracy score to evaluate the performance of the model.\
Based on our modeling process, the best model was a Tuned Logistic Regression model with added Tweet and has an accuracy of 87%.
```
# Define the pipeline with TF-IDF vectorizer and Logistic Regression classifier
pipeline_logreg_best2 = Pipeline([
    ('tfidf', TfidfVectorizer(stop_words=stopwords_list)),  # Vectorize the text data using TF-IDF
    ('logreg_classifier', LogisticRegression(C=1, class_weight='balanced', max_iter=100, solver='liblinear'))  # Logistic Regression classifier with best parameters
])

# Train the pipeline
pipeline_logreg_best2.fit(X_train2, y_train2)
# Evaluate the model
y_pred_logreg_best2 = pipeline_logreg_best2.predict(X_test2)
print(classification_report(y_test2, y_pred_logreg_best2))
```
## Conclusion

By implementing NLP techniques to dissect negative sentiment surrounding Apple products at the 2013 SXSW Conference, this analysis offers valuable insights essential for strategic decision-making. Through a nuanced understanding of consumer sentiment, Apple can refine its products, communication strategies, and customer interactions to foster enhanced brand loyalty and satisfaction.\
Based on our NLP analysis of negative sentiment on Apple products during the 2013 SXSW Conference on Twitter, the following conclusions can be drawn:

1. Users frequently criticized the designs and battery life of Apple products.
2. A common source of frustration among consumers regarding the performance of Apple devices was related to apps and battery life.
3. The primary concerns raised by users regarding aesthetics and user interface were related to designs and apps.
## For More Information

Please review our full analysis in jupyter notebook ([NLP Analysis for Apple product](https://github.com/ermiyas-sidama/KET-NLP-Analysis-For-Apple-Product/blob/main/KET-NLP-Analysis-For-Apple-Product.ipynb))\
And also refer to our 
- ([Presentation](https://www.canva.com/design/DAGEpfKhGSA/70EH7vs7p4lsmEqbvKAyvA/edit?utm_content=DAGEpfKhGSA&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)) 

## Contributors

([Ermiyas Sidama](https://github.com/ermiyas-sidama))
([Karina Baculima](https://github.com/karisteph ))
([Travis Clark](https://github.com/TravisClark1432 )) 

## Repository Structure

```
|— README.md                                                 <- The top-level README for reviewers of this project
|— KET-NLP-Analysis-for-Apple-product.ipynb                  <- Interactive computing environment including analysis in Jupyter notebook
|— KET-NLP-Analysis-for-Apple-product-Repo.pdf               <- PDF version of Repo
|_ KET-NLP-Analysis-for-Apple-product-presentation.pdf       <- PDF version of project presentation                                               |— KET-NLP-Analysis-for-Apple-product-JupyterNotebook.pdf    <- PDF version of Jupyter Notebook                                                  
|— .gitignore                                                <- gitignore exclude selected file execute
|— Data                                                      <- Source data
    |— judge-1377884607_tweet_product_company.csv            <- Raw data

```
       

