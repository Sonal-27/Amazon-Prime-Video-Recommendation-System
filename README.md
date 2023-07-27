# Amazon-Prime-Video-Recommendation-System

## ABSTRACT
In recent years, recommendation systems have evolved as a solution to the problem of information overload by presenting users with the most appropriate products from a vast amount of data. The goal of online collaborative movie ideas for media products is to assist customers in obtaining their favorite films by pinpointing precisely identical people or films from their prior shared searches. The lack of data makes neighbor choosing more difficult with the rapid development of movies and consumers. This study demonstrates the capability of ML models to recommend the user with the top 5 recommendations when the user starts searching for a particular movie or TV-show with respective to its genre, description, cast, director, etc. In particular, four standards models, such as KNN, Gaussian Naive Bayes, Complement Naive Bayes, and Bernoulli Naive Bayes have been used in this study.

## KEYWORDS
**Datamining:** Data extraction has become incredibly difficult. Because of the large size of the data set, traditional data analysis tools and methodologies are frequently ineffective. As a result, we employ data mining technology. Data mining is the process of identifying usable information in massive data sources automatically. To improve information retrieval systems, data mining methods have been used.

**Dataset:** It is a collection of data.

**Data Preprocessing:** The goal of preprocessing is to convert raw input data into a format suited for further analysis. It entails combining data from several sources, cleaning the data to reduce noise and duplicate observations, and picking records and features.

**Machine learning:** Machine learning is a branch of artificial intelligence that is widely described as a machine's ability to mimic intelligent human behavior.

**Recommendation System:** A recommender system, often known as a recommendation system (occasionally replaced by a synonym such as platform or engine), is a type of information filtering system that provides suggestions for items that are most relevant to a certain user.

## INTRODUCTION
Due to the rise of websites like YouTube, Amazon, Netflix, and many others over the past couple decades, recommender systems have become more and more common in our lives. Whether it is in e-commerce (which suggests to customers articles that may interest them) or online advertising, recommender systems are becoming an essential component of our daily online activity (suggest to users the proper contents, matching their tastes). Recommender systems are really critical in some industries as they can generate a huge amount of income when they are efficient or also be a way to stand out significantly from competitors. In this study, we will use various machine learning models to provide the top 5 recommendations to the user when they begin looking for a specific movie or TV show based on the genre, summary, cast, director, etc. This study has specifically used four standard models KNN, Gaussian Naive Bayes, Complement Naive Bayes, and Bernoulli Naive Bayes.

**About the dataset:** This data set contains a list of all shows available for streaming on Amazon Prime. This data was obtained in May 2022 and contains data that is available in the United States.

## Methods
We propose building the system on Collaborative and Content-based filtering technique for recommendation system. In our proposed methodology, there are four main components that are

##### 1. Data Preprocessing
##### 2. Data Visualization
##### 3. Feature extraction
##### 4. Model implementation
##### 5. Accuracy metrics

### Data Preprocessing:

**Step 1:** Reading the CSV file.

**Step 2:** Removed null values present in the dataset for attributes country, date added, rating by using mode values of that specific column. Removed rows of cast and directors having null values

**Step 3:**  Removed stop words.

### Data Visualizations:
- visualized genres based upon on count (i.e, Movies/Tv Shows)
- Generated Top 5 Actors in the data set.
We have generated rating of different contents on the data set.
We have generated top 5 directors in the data set.
We have also generated Genres by Countries.

### Feature Extraction:
- **Tokenization:** It is the process of segmenting a stream of text into “tokens,” which are words, symbols, and other meaningful components. This is done so that we can consider the tokens as separate parts that combine to create a title, description, cast name, or director name.
- **Stop Word Removal:** Stop words are a category of extremely common expressions that, when used in a text, are considered useless because they don’t add any new information. Examples include, among others, “a", "an," "the," "he," "she," "by," and “on."
- **TF-IDF:** The TF-IDF statistic gauges a word's applicability to a particular document or set of documents (term frequency-inverse document frequency). It was initially made for searching and recovering documents. But over time, it has also been utilized in recommendation engines and machine learning models.
- **Count Vectorizer:** A given text is converted into a vector using the frequency (count) of each word in the full text. This is useful when we have several such texts and want to make each word into a vector (for using in further text analysis).
 
### Model Implementation:
- **Content-Based Filtering:** Content-based filtering is a form of recommender system that attempt to estimate what a user may like based on previous behavior. By matching keywords and attributes assigned to objects in a database (for example, items in an online marketplace) to a user profile, content-based filtering generates recommendations. Data acquired from a user's actions, such as purchases, ratings (likes and dislikes), downloads, products searched for on a website and/or placed to a basket, and product link clicks, are used to build the user profile.
- **Collaborative-Based Filtering:** Collaborative filtering is a technique that employs the reactions of other users to filter out items that a user may be interested in. It functions by searching a large group of people for users who have similar interests to a given user. It considers the products they like and combines them to get a ranked list of recommendations.
- **KNN:** The k-nearest neighbors’ algorithm (k-NN) was developed by Evelyn Fix and Joseph Hodges in 1951 and was later enhanced by Thomas Cover. It is a non-parametric supervised learning method. Regression and classification are two of its uses. A data collection's k closest training examples serve as the input in both scenarios. KNN is an excellent go-to model for implementing item-based collaborative filtering, as well as a solid foundation for developing recommender systems. KNN makes no assumptions about the underlying data distribution, instead relying on item feature similarity.
- **Naive Bayes:** Simple "probabilistic classifiers" known as "Naive Bayes classifiers" makes use of the Bayes theorem and build stronger (naive) assumptions about the independence of the characteristics (see Bayes classifier). Since a Naive Bayes text classifier is based on the Bayes' Theorem, which lets us to compute the conditional probability of occurrence of two events based on the probabilities of occurrence of each individual event, encoding those values is incredibly useful.
 
#### Types of Naïve bayes:
- **Gaussian Naive Bayes:** In Gaussian Naive Bayes, a Gaussian distribution for the continuous values of each feature is taken for granted. The Gaussian distribution is sometimes known as the Normal distribution. When the feature values are plotted, it produces a bell-shaped curve that is symmetric around the mean of the feature values.
- **Complement Naive Bayes:** Complement Naive Bayes is a modification of the Multinomial Naive Bayes method. Unbalanced datasets behave badly with Multinomial Naive Bayes. A dataset that is imbalanced has more samples of one class than any other class. This demonstrates that the sample distribution is inconsistent. Instead of calculating the likelihood of an item belonging to a certain class, we calculate the chance of the item belonging to all classes in complement Naive Bayes. Complement Naive Bayes is named after the literal meaning of the word, complement.
- **Bernoulli Naive Bayes:** The features of the multivariate Bernoulli event model are independent Booleans (binary variables) that describe inputs. This model is widely employed for document classification problems in place of term frequencies, where binary term occurrence characteristics (whether a word appears in a document or not) are used (i.e., frequency of a word in the document).

## RESULTS & CONCLUSION

For recommending movies by using cosine similarity with tf-idf vectorizer gave us 1 similarity and with count vectorizer we got good similarity which is greater than 0.7.

For KNN model we have obtained 74% accuracy with top 5 recommendations. For Naïve bayes models we have obtained 79% accuracy for both Complement Naïve Bayes, Bernoulli Naïve Bayes and for Gaussian Naïve Bayes we have obtained 68% accuracy.

Therefore, we conclude that Complement Naïve Bayes and Bernoulli Naïve Bayes performs better with an accuracy of 79% when compared to KNN Classifier and Gaussian Naïve Bayes.
