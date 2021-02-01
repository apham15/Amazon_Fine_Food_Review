# Amazon_Fine_Food_Review
[Amazon.com, Inc.](https://www.amazon.com/) is an American multinational technology company based in Seattle, Washington, which focuses on e-commerce, cloud computing, digital streaming, and artificial intelligence. The fine food data span a period of more than 10 years, including all ~500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plaintext review.
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
* Model-based Collaborative Filtering is a personalised recommender system, the recommendations are based on the past behavior of the user and it is not dependent on any additional information.
* Based on the real value and the predict value, it is clear to see that the predictive recomendation system is great
* The Popularity-based recommender system is non-personalised and the recommendations are based on frequecy counts, which may be not suitable to the user.You can see the differance above for the user id 70 and 100, The Popularity based model has recommended the same set of 5 or 6 products to both but Collaborative Filtering based model has recommended entire different list based on the user past purchase history
