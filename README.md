# Amazon_Fine_Food_Review
[![Run in Google Colab](https://img.shields.io/badge/Colab-Run_in_Google_Colab-blue?logo=Google&logoColor=FDBA18)](https://colab.research.google.com/drive/152Bde9BARD6lZczGvFlDGL91nATMPRRl?usp=sharing)
[![Open Notebook](https://img.shields.io/badge/Jupyter-Open_Notebook-blue?logo=Jupyter)](https://github.com/apham15/Amazon_Fine_Food_Review/blob/main/amazon%20food%20review.ipynb)


[Amazon.com, Inc.](https://www.amazon.com/) is an American multinational technology company based in Seattle, Washington, which focuses on e-commerce, cloud computing, digital streaming, and artificial intelligence. The fine food data span a period of more than 10 years, including all ~500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plaintext review.
![31d13c99ee841869ca44ef54ba956272](https://user-images.githubusercontent.com/63126292/106423731-a550c180-6426-11eb-84a7-ca4f738f5ae2.png)

## 1. What are the target of this project?
* Analyzing the top review, top product, top user for fine food
* Applying Sentiment Analysis to analyze the plaintext review
## 2. My solution
a. Create a Recommendation system based on Sparse Matrix for fine food
* EDA based on UserId, ProductId, HelpfulnessNumerator, HelpfulnessDenominator, Score, Time
* Utilizing Descriptive Analysis
* Applying Sparse Matrix to define the recommended selection
* Evaluating my recommdation system with MSE

b. Sentiment Analyse
* EDA / Text cleaning
* Applying BoW, Word2Vec, and TD-IDF as a feature engineering to vectorize the text
* Applying machine learning algorithms model (Bernoulli Naive Bayer, Logistic Regression) to predict the sentiment
* Evaluating model based on log loss and accuracy scores
* Selecting top words by apply K-means clustering method and plot it 2d and 3d with plot ly and t-SNE dimensionality reduction
* Utilizing text preparation with Keras and applying deep learning (ANN and RNN-LSTM)
* Evaluating model based on log loss and accuracy score
## 3. Outcome
a. Recommendation system with Sparse Matrix ```scipy.sparse.linalg.svds```

a.1. Building Popularity Recommender system

![Screen Shot 2021-02-01 at 12 18 47 AM](https://user-images.githubusercontent.com/63126292/106421861-1c845680-6423-11eb-806f-18718e28b9ff.png)

* Since this is a popularity-based recommender model, recommendations remain the same for all users
* We predict the products based on the popularity. It is not personalized to particular user

a.2. Building Collabrating Filtering
* Model-based Collaborative Filtering is a personalised recommender system, the recommendations are based on the past behavior of the user and it is not dependent on any additional information.

![Screen Shot 2021-02-01 at 12 13 01 AM](https://user-images.githubusercontent.com/63126292/106421595-9a942d80-6422-11eb-8261-6f57cfae269b.png)
![Screen Shot 2021-02-01 at 12 12 54 AM](https://user-images.githubusercontent.com/63126292/106421671-bc8db000-6422-11eb-9855-b83303eafce4.png)

* Based on the real value and the predict value, it is clear to see that the predictive recomendation system is great
* The Popularity-based recommender system is non-personalised and the recommendations are based on frequecy counts, which may be not suitable to the user.You can see the differance above for the user id 70 and 100, The Popularity based model has recommended the same set of 5 or 6 products to both but Collaborative Filtering based model has recommended entire different list based on the user past purchase history

b. Sentiment Analysis

b.1 Machine Learning Algorithms

* [Accuracy]![Screen Shot 2021-02-01 at 12 20 48 AM](https://user-images.githubusercontent.com/63126292/106421972-5fdec500-6423-11eb-9edf-4e5de62c1a93.png)
* [Log Loss]![Screen Shot 2021-02-01 at 12 20 55 AM](https://user-images.githubusercontent.com/63126292/106422031-79800c80-6423-11eb-816b-c85973174c77.png)

* TF-IDF is the best model that has the highest accuracy score for both NernoulliNB and Logistic regression

![Screen Shot 2021-02-01 at 12 26 21 AM](https://user-images.githubusercontent.com/63126292/106422417-2a86a700-6424-11eb-9090-13ce94a73037.png)

* Logistic Regresison is the best model that fit in this dataset because it bring the highest accuracy score with the lowest log loss
* Tuning model, the best parameters set fo Logistic Regression is ```lr__C: 100.0, 	lr__penalty: 'none', lr__solver: 'saga'```
b.2 Clustring the top words with K-mean
* The best number of cluster is 3 with the highest Silhoutte Score is 0.002
* Top 10 words are ['strong', 'br', 'cup coffee', 'tea',  'taste',  'like', 'cups', 'flavor', 'coffee', 'love', 'one', 'food', 'good', 'cup', 'great', 'bold', 'br br', 'product']

![newplot](https://user-images.githubusercontent.com/63126292/106422475-438f5800-6424-11eb-8abb-936c32d58c9f.png)

b.3 Deep Learning
* Developing both ANN and RNN-LSTM, LSTM is the best one with the best accuracy score is 96%

![download](https://user-images.githubusercontent.com/63126292/106423195-961d4400-6425-11eb-8ad6-291f80cf2f04.png)
![download (1)](https://user-images.githubusercontent.com/63126292/106423224-a6352380-6425-11eb-8ad2-b924ba4855b8.png)

##4. Conclusion
* Amazon Fine Food Review dataset is the credible one. It allows me to utilized all my skills: statistical analysis, supervised learning method, unsupervised learning method, machine learning algorithm, deep learning. 
* From this dataset, I learn that with deep learning, everything is so simple. Kereas class with tokenzie to vectorize word is faster than TF-IDF traditional method. Also, RNN-LSTM utilized the plaintext review vectorized to bring up the better accuracy score for future sentiment analysis
* My work is useful for all type of e-commerce because it can apply for both strategy team and customer service team to help the business to be better.
