# NLP Analysis for Apple product
## Introduction
In todays digital world social media plays a vital role in collecting data .Twitter is one of the social media which  has a huge sources of consumers opinion and sentiments. Analyzing these data using Natural Language Processing(NLP) techniques offer valuable insight in to public perceptions of brands and products.This introduction outlines the process of conductingNLP analysis for apple product sentiment on Twitter.\
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
The dataset comes from CrowdFlower ([Data.World](https://data.world/crowdflower/brands-and-product-emotions)) Human raters rated the sentiment in over 9,000 Tweets as positive, negative, or neither.
In this project we focused on positive and negative sentiment. 
![image](https://github.com/ermiyas-sidama/NLP-Analysis-for-Apple-product/assets/160514617/b294e3fb-e00d-46cf-b376-e9fc684769d9)
The figure above shows that the data is Class Imbalance. As result we will augment our dataset by adding additional negative tweets. This strategy aims to provide the model with more representative examples of negative sentiments, thereby improving its ability to accurately classify negative tweets. 


## Methods

## Analysis / Modeling


## Conclusion
Based on our NLP analysis of negative sentiment on Apple products during the 2013 SXSW Conference on Twitter, the following conclusions can be drawn:

1. Users frequently criticized the designs and battery life of Apple products.
2. A common source of frustration among consumers regarding the performance of Apple devices was related to apps and battery life.
3. The primary concerns raised by users regarding aesthetics and user interface were related to designs and apps.

## For More Information
Please review our full analysis in jupyter notebook ([NLP Analysis for Apple product](https://github.com/ermiyas-sidama/NLP-Analysis-for-Apple-product/blob/main/README.md))\
And also refer to our 
- ([Presentation](https://docs.google.com/presentation/d/1ijBPPvqfAkNkCyVd-PAvYYbMsxsdxGZkPknvgijaI1o/edit#slide=id.g2da3e7edccf_0_1)) 

## Contributors
([Ermiyas Sidama](https://github.com/ermiyas-sidama))
([Karina Baculima](https://github.com/karisteph ))
([Travis Clark](https://github.com/TravisClark1432 )) 
## Repository Structure
```
|— README.md                                                 <- The top-level README for reviewers of this project
|— NLP_Analysis_for_Apple_product.ipynb                      <- Interactive computing environment including analysis in Jupyter notebook
|— .gitignore                                                <- gitignore exclude selected file execute
|— Data                                                      <- Sourced externally 
    |— judge-1377884607_tweet_product_company.csv            <- Raw data
|_ presentation.pdf                                          <- PDF version of project presentation
```

