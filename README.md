# Knn-on-amazon-fine-food-reviews
Given a review, Using Knn model determine whether the review is positive (rating of 4 or 5) or negative (rating of 1 or 2).   
[Q] How to determine if a review is positive or negative?  
[Ans] We could use Score/Rating. A rating of 4 or 5 can be cosnidered as a positive review. A rating of 1 or 2 can be considered as negative one. A review of rating 3 is considered nuetral and such reviews are ignored from our analysis. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.

Models used:
  Sklearn Knn classifier - brute and Kdtree algorithms 
Vectorizers used :
  Bow (sklearn-CountVectorizer),Tfidf(sklearn-TfidfVectorizer),Avg-W2v(trained a gensim model),Tfidf-W2v
Metrics used:
  auc(sklearn's roc_auc) and Accurcy

Obtained results:

+------------+------------+----+----------+-----------+
| Vectorizer |   Model    | K  | Accuracy | AUC score |
+------------+------------+----+----------+-----------+
|    BOW     | Knn-Brute  | 10 | 82.3529  |    0.81   |
|   Tfidf    | Knn-Brute  | 10 | 85.66673 |    0.8    |
|  Avg-W2V   | Knn-Brute  | 10 | 87.6564  |    0.89   |
| Tfidf-W2v  | Knn-Brute  | 10 | 86.2889  |    0.85   |
|    BOW     | Knn-Kdtree | 10 | 82.5844  |    0.81   |
|   Tfidf    | Knn-Kdtree | 12 |  83.532  |    0.83   |
|  Avg-W2v   | Knn-Kdtree | 10 | 87.3453  |    0.89   |
| Tfidf -w2v | Knn-Kdtree | 10 | 86.2745  |    0.85   |
+------------+------------+----+----------+-----------+
