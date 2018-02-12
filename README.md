# Suicidal Ideation Detection in Online User Contents

# Getting Started
Due to the anonymity of online media and social networks, people tend to express their feelings and sufferings in online communities.
In order to prevent suicide, it is necessary to detect suicide-related posts and users' suicide ideation in cyberspace by natural language processing methods.
We focus on the online community called Reddit and the social networking website Twitter, and classify users' posts with potential suicide and without suicidal risk through texts features processing and machine learning based methods.


# Datasets
We collect two sets of data from Reddit and Twitter.
The Reddit data set includes 3,549 suicidal ideation samples and a number of non-suicide texts (20k). The Twitter dataset has totally 10k tweets with 594 tweets (around 6\%) with suicidal ideation.

The Reddit word cloud (left) and Twitter word cloud (right) are shown as follow:

<img width="400" alt="Reddit word cloud" src="https://github.com/shaoxiongji/sw-detection/blob/master/output/reddit.jpg"><img width="400" alt="Twitter word cloud" src="https://github.com/shaoxiongji/sw-detection/blob/master/output/twitter.jpg">

However, original text data can not be provided for the consideration of users privacy.
If you'd like to collect data, please refer this repository: [web spider](https://github.com/shaoxiongji/webspider-eda).
These two xlsx files in this project contain some sample data composed by the author.
*Notice: when running the scripts, please replace them with your own data.*

# Features Precessing
We extracted six sets of features, i.e., statistical features, POS counts, TF-IDF, Topics probability, [LIWC](http://liwc.wpengine.com), and pre-trained [word2vec](https://radimrehurek.com/gensim/models/word2vec.html) word embedding.

The csv files are the processed features using [LIWC](http://liwc.wpengine.com).
*Notice: when running the scripts, please replace them with your own data.*

All these features are visualized in the following 6 pictures, using PCA as dimensionality reduction.

<img width="500" alt="features" src="https://github.com/shaoxiongji/sw-detection/blob/master/output/all.png">

# Running the scripts
Six models were implemented. They are logistic regression, random forest, gradient boosting decision tree, xgboost, support vector machine, and LSTM networks.

Former five models for Reddit and Twitter were implemented by
`python clf.py`
and
`python clf_reddit.py`.
The LSTM model for Reddit and Twitter by
`python lstm.py` and `python lstm_reddit.py`.
`python lstm_word2vec.py` and `python lstm_word2vec_reddit.py`.

These scripts were written in Python 3.6. Please check the requirements before running.
