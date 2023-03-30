# Phase_4_Final_Project

## BUSINESS PROBLEM UNDERSTANDING

This analysis aims to build NLP binary classifier to analyze positive, negative and neutral Twitter sentiment about Apple and Google products.
Stakeholders who could benefit having this information are consumers, the companies themselves (engineers and tech professionals working on the products and the services provided with them), investors and partners as they can be used as insights to improve the customers experience.

## What is Twitter?
Twitter is an online social media and social networking service performed by micro blogging in real time.

## Models

Chosen models are:

- Gaussian NB.
- Random Forest.
- Support Vector Machine.

## Evaluation

Chosen metric: 

- Precision.
- Recall.
- F1 score.
- Accuracy score. 
- AUC ROC scores.

## DATA PROCESSING 

DATASET DESCRIPTION

It was provided through DataWorld website.
The dataset chosen for this analysis consists of 9093 entries, spread on 3 columns. Values are tweets expressed positive, negative, or no emotion towards products branded Apple and Google.
Given the nature of the entries, data type is obj for all three features. In this case, the rating system, even though it is encoded, it is still an obj data.
It would have been interesting for a more targeted analysis and the identifications of patterns the inclusions of demogrophical data.
Brief columns description:
Column labels are understandable even though not straightforward. Thus, a more clear labeling is needed.
Issues like missing values are already identifiable given the summary showed by the info.

Data cleaning is needed:
- Deleting missing values.
- Deleting punctuation, stopwords, HTML and non ASCII characters, numbers. 
- Lowercase formatting.
- Dropping of rows not necessary for the analysis.
- Reclassifying emotion and products nomenclature.

## EXPLORATIVE DATA ANALYSIS

I start the EDA with some basic views of the numbers related to the products and the reactions and plotting the results.

Percentages related to the posts.

![IMAGE1](https://user-images.githubusercontent.com/16385415/228739369-df32f316-bc63-4cbf-8817-7bcbea8f67a9.png)

![IMAGE2](https://user-images.githubusercontent.com/16385415/228739430-5c3bc003-6d3d-4dc2-906a-a173d767e6aa.png)

Words analysis results, respectively positive and negative, for Apple.

<img width="943" alt="IMAGE3" src="https://user-images.githubusercontent.com/16385415/228739676-91cc5c52-4c80-4037-a024-b0751b8a577d.png">

<img width="943" alt="IMAGE4" src="https://user-images.githubusercontent.com/16385415/228739822-c0da4751-28e3-4b85-b83b-0c8668e83b0a.png">

Words analysis results, respectively positive and negative, for Google.

<img width="936" alt="IMAGE5" src="https://user-images.githubusercontent.com/16385415/228740110-d557deea-96ed-4a84-913e-3c8c0cd360b4.png">

<img width="936" alt="IMAGE6" src="https://user-images.githubusercontent.com/16385415/228740185-10926eb1-2fd6-4b5e-9a24-627297857106.png">

## BINARY CLASSIFICATION
I proceed with the modeling process with the chosen algorythms.

<img width="548" alt="IMAGE7" src="https://user-images.githubusercontent.com/16385415/228740750-59df1381-bbea-43f7-93a7-2cd7f776b139.png">

<img width="553" alt="IMAGE8" src="https://user-images.githubusercontent.com/16385415/228740804-2c72c9ef-83d5-4933-882e-7bcc3c2c7573.png">

<img width="562" alt="IMAGE9" src="https://user-images.githubusercontent.com/16385415/228740856-c8b98b09-6e4b-443c-8355-6fa480306500.png">

# RESULTS DISCUSSION

## TEXT ANALYSIS

It is possible to assess the vast majority of the tweets are positive 84%, over 16% negative.
Apple and its products have the majority of mentions with 28.8% (ipad), 19.1% (apple), 14.2% (ipad and iphone app); Google appears with 14.9%.
As it is possible to assess from the plots most the vast majority of the posts related to the brand and their products are negative.
For APPLE POSITIVE TWEETS Most frequent words are related to SXSW conference and the pop up stores and the presentation of the new iPad 2 and the iPhone their features like design, case and app, free.
For APPLE NEGATIVE TWEETS With the mention again to the SXSW conference, some features are highlighted like battery, button, design, headaches or adjectives like tap worthy, fascist.
For GOOGLE POSITIVE TWEETS There’s a reference to the SXSW conference while other remarks are network, panel, doodle, party while among its products android and maps occur.
For GOOGLE NEGATIVE TWEETS With the same reference to the SXSW conference the words appearing are fail, network, circle, launch, business, maps, location, service, social, bing and android.


# RESULTS DISCUSSION

### TEXT ANALYSIS

It is possible to assess the vast majority of the tweets are positive 84%, over 16% negative.

Apple and its products have the majority of mentions with 28.8% (ipad), 19.1% (apple), 14.2% (ipad and iphone app); Google appears with 14.9%.

As it is possible to assess from the plots most the vast majority of the posts related to the brand and their products are negative.

For APPLE POSITIVE TWEETS
Most frequent words are related to SXSW conference and the pop up stores and the presentation of the new iPad 2 and the iPhone their features like design, case and app, free. 

For APPLE NEGATIVE TWEETS
With the mention again to the SXSW conference, some features are highlighted like battery, button, design, headaches or adjectives like tap worthy, fascist.

For GOOGLE POSITIVE TWEETS
There’s a reference to the SXSW conference while other remarks are network, panel, doodle, party while among its products android and maps occur.

For GOOGLE NEGATIVE TWEETS
With the same reference to the SXSW conference the words appearing are fail, network, circle, launch, business, maps, location, service, social, bing and android.


## MODELING ANALYSIS

Accuracy is the metric generally used to evaluate and compare models. It is calculated by the total number of true positives and true numbers are divided by the total number of observations.
In this case it is possible to state that:
    
- Gaussian NB: 0.95
    
- Random Forest: 0.87
    
- Support Vector Machine: 0.94
    
Accuracy though, can be misleading and it is advisable to consider the other metrics provided, according to the best suitable business scenario.


Given the values assigned in 
    
- True Negatives are the negative tweets correctly identified as negative.

- False negatives are the positive tweets, uncorrectly identified as negative

- True positive are the positive tweets correctly identified as positive.

- False positive are the negative tweets uncorretly identified as positive.


Which customers are important to this company?

False Negatives and False Positives, and specifically False Positives. It is imperative for business companies that rely on "words of mouth" and reviews to engage customers, acquiring new ones and retaining the existing one, to address negative comments, accusations or features. They could potentially damage their reputation and image, two elements for which time and consistency are absolutely necessary.

Given that, it is more important to consider precision and AUC&ROC score.

- Precision. Out of the tweets that the model predicted would be positive, they are actually positive:

    - Gaussian NB: 87%
    - Random Forest: 42%
    - Support Vector Machine: 97%


- ROC and AUC. 

ROC summarizes the performance of a binary classification model on the positive class. AUC function takes both the true outcome from the test set and the predicting set for the positive class.
Support Vector Machine: the model performs almost perfectly discriminating True Positive and False Positive.


I can examine the other metrics as well: 

- Recall. 
Out of all the tweets that are actually positive, the model only predicted this outcome correctly for those:

    - Naive Gaussian Bayes: 97%
    - Random Forest: 61%
    - Support Vector Machine: 80%


- F1 Score. 
This metric indicates how well the model predicts the churning choice. The closer the value is to 1, the better the model performs. Examining the values:

    - Naive Gaussian Bayes: 0.91
    - Random Forest: 0.46
    - Support Vector Machine: 0.93



# CONCLUSION

## TEXT ANALYSIS

The classification of positive and a negative tweets used a tool for the business seemed to be confirmed. 
It consists in the millions of pairs of fresh eyes that scrutinize company and their products, services and reputation and led not only improvements but also innovation, being Twitter a direct line for customer engagement.
Comparing Apple and Google it seems like there is a major focus on the products for Apple, on the community for Google.
However Apple is named as fascist.

## MODELING ANALYSIS

According to the interpretation of these results, among the models used to solve this business problem for Apple and Google, it can be stated that the Support Vector Machine is the model that performs best as a classifier for this dataset, in order to predict the positive and negative reactions of customers based on sentiment analysis of their tweets. 

As the matter of fact, the Support Vector Machine model was able to predict correctly positive tweets with very high degree (precision: 96%, recall 80%, F1 score 93%) results. This trend is also confirmed by the ROC plots which returns a almost perfect capability of identification.

## RECOMMENDATIONS

- Users seems to complain about: 
    - Iphone's usability features and related performance like for battery
    - Ipad design
    - Android apps
    - Google maps and network.
    
It would advisable to focus on improving these items.

Alternative forms of customer engagement like conferences, parties and pop stores are highly appreciated. For this reason, it would be recommendable to keep investing on this line.











