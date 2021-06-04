# Sentiment-Analysis-of-Amazon-Alexa-Reviews

# Introduction
Background: The public relations department team has collected extensive data on their customers such as product reviews. Based on the reviews (in text format), the team would like to predict whether their customers are satisfied with the product or not. 

Data: The dataset consists of 3150 Amazon customer reviews for Alexa Echo, Firestick, Echo Dot, etc.

# Methodology
Since this is a binary classification problem, I applied two classic NLP models, Naive Bayes classification and logistic classification. The primary metric would be the accuracy.

# EDA

The dataset includes 3150 rows and 5 columns, while the last column is the response variable. (Note: 1 indicates the positive feedback)
![dataset](https://user-images.githubusercontent.com/64850893/104144804-c592e080-5392-11eb-8a1d-dcbf910bfe79.jpg)

As for the distribution of the feedback, most of them are positive feedbacks.
![feedback](https://user-images.githubusercontent.com/64850893/104144920-30dcb280-5393-11eb-9e34-ffa24da380e4.jpg)

Another straightforward way to check the overall sentiment of the reviews is the WordCloud.
![cloud](https://user-images.githubusercontent.com/64850893/104144939-3d610b00-5393-11eb-813f-ee133a9552ce.jpg)



# Date Cleansing
1. Remove the punctuation.  

2. Remove the stopwords.

3.  Perform count vectorization(tokenization). 

The clean dataset is the following dataset with the shape of 3150 * 5227.

![clean](https://user-images.githubusercontent.com/64850893/104145301-6930c080-5394-11eb-856f-965ce9caa6a0.jpg)


# Model 1 - Naive Bayes Classifier

Confusion Matrix:

![nb_result](https://user-images.githubusercontent.com/64850893/104147965-5fac5600-539e-11eb-87f3-5eadc58a780d.jpg)

Metrics Table:

![nb_table](https://user-images.githubusercontent.com/64850893/104147977-6c30ae80-539e-11eb-9bb1-8ccd746921fe.jpg)

# Model 2 - Logistic Classifier

Confusion Matrix:

![log_result](https://user-images.githubusercontent.com/64850893/104147998-7c488e00-539e-11eb-9578-d7f896be6533.jpg)

Metrics Table:

![log_table](https://user-images.githubusercontent.com/64850893/104148004-84a0c900-539e-11eb-8859-6ebc84ab82a7.jpg)

# Conclusion

1. Both models achieve about 91% of prediciton accuracy.

2. However, the precision and recall for the negative feedback class are relatively low, while those metrics for the positive feedback are close to 100%.

# Future

1. Experiment more kinds of NLP Models.

2. Implement sampling methods to deal with the imbalanced class.
