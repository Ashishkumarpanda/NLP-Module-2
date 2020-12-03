# How To Use Scikit-Learn in NLP?

**Scikit learn is a library used to perform machine learning in Python. Scikit learn is an open source library**.
### while performing an NLP task there are three things that needs to be modified
* The words of the data
* The obtained words in to their vector form
* Then putting them in a stack and predict accordingly

### Basically sentiment analysis catagorized those provided data into negative or positive half .
<img src="https://s3.amazonaws.com/stackabuse/media/python-nlp-sentiment-analysis-scikit-learn-3.png"></img>

*Now let's get started with how to implement this on any given dataset*
## importring required libraries from scikit-learn
* `import numpy as np`
* `import pandas as pd`
* `import re`
* `import nltk` 

## importing the dataset

* `data_source_url = "data.csv"`
* `data = pd.read_csv(data_source_url)`

## Data preprocessing will be done according to the given dataset, like removal of null or zero values or normalization etc according to the data provided.

## removal of stop words from a sentence

* `nltk.download('stopwords')`

* `ps=PorterStemmer()`
 * `corpus=[]`
 * ` for i in range(len(message)):`
 * `review=re.sub('[^a-zA-Z]',' ',message['title'][i])`
  * `review=review.lower()`
 * `review=review.split()`

 * `review=[ps.stem(word) for word in review if not word in stopwords.words('english')]`
 * `review=' '.join(review)`
 * ` corpus.append(review)`
 
 ### This will give you the list of sentences preprocessed so that it can be converted in to the vector form which can be done by using one_hot and pad_sequences provided in the keras.
 <img src = "https://cdn-images-1.medium.com/max/1600/1*svLRt3OwVyqZiyDammWqiA.png"></img>
 
 After getting these now we wil divide the dependent and independent variables and can predict accordingly
  
