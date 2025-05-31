# 🎬 Movie Reviews Sentiment Analysis

This project performs sentiment analysis on movie reviews to classify whether a given review expresses a positive or negative opinion. The analysis involves text preprocessing, tokenization, stopword removal, vectorization, and classification using machine learning models.

## 🗃️ Dataset

The dataset contains textual movie reviews labeled with sentiment:
- review: Free-text movie review
- sentiment: Binary label (0 = negative, 1 = positive)

## 🧹 Preprocessing

-Remove HTML tags
-Remove special characters
-Convert everything to lowercase
-Remove stopwords
-Stemming
- Tokenized reviews using `word_tokenize`
- Vectorized text using `TfidfVectorizer`
- Converted labels to numeric binary format

## 🧠 Model Training
The project uses three variants of the Naive Bayes algorithm to classify the sentiment of movie reviews:
Models Trained:
-GaussianNB() – for continuous features (not ideal for sparse text data, but tested)
-MultinomialNB() – best suited for text classification with word counts or TF-IDF
-BernoulliNB() – works well with binary/boolean feature vectors (e.g., word presence)


## 📈 Results

🔵 Bernoulli Naive Bayes (BNB) achieved the highest accuracy, making it the best-performing model for this binary sentiment classification task. Its ability to handle binary features (word presence/absence) aligns well with TF-IDF’s sparsity.
🟡 Multinomial Naive Bayes (MNB) closely followed, performing strongly with frequency-based inputs. This model is commonly used in NLP and remains a reliable option.
🔴 Gaussian Naive Bayes (GNB) underperformed due to its assumption of normally distributed continuous features, which does not match the sparse, high-dimensional structure of TF-IDF vectors.
•	For TF-IDF-based sentiment classification, BernoulliNB slightly outperforms MultinomialNB.
•	GaussianNB is not recommended for text data unless feature engineering transforms the data to continuous distributions.
