# Spooky Author Data
Import Required Libraries
df_train will contain the train information
df_test will contain the test information**

The id column is a unique value that identified the row. We will discard this for our predictions.
The text column contains some text written by a specific author.
The author column, contains a string, that's identifies the author that wrote the text. This is the value that we will use to train our model and let it know to whom it corresponds, so that when me make the predictions, our model will know what values to predict.

Removing punctiation is important when you work with text, since you don't want your predictions to take special characters like '.', ',' or ':' into account.

On this cell, I'll show you how to make this removal by hand, even though there are many libaries to do this (including NLTK).

The punctuation attribute in string.punctuation contains a list of punctuations so we don't have to type them by hand.

#Stemming
Stemming is the process of converting words that mean the same. For example, verb conjugation. Words like run, running, ran, all are the same word on different conjugations

Vectorization¶
One of the most common feature engineering when dealing with text, it's vectorization.
On this notebook we will make use of two different implementations: Count Vectorizer and TfidfVectorizer¶

Both work by counting each word on a corpus of text, so here I will show code for each one, but both have the same following parameters which are important to understand:

Stop Words¶
Finally, the stop words parameter will let us remove the stop words such as the, a, and, or, etc.... We can pass the name of the language (scikit learn only comes with english by default) or a list of words, on our example, we will use english.

Split Train and Test for validation

Multinomial Naive Bayes¶
Multinomial Naive Bayes is one of the most common algorithm used in text clasification, so we will work with it.
 
Predict test values¶
Once we have our model trained, we can predict the test values, and then compare them to the real values.

Next step is validate the model. We will import the accuracy_score function of sklearn, to see how is our accuracy
A confusion matrix is a matrix where we can see where the predicted values are, and where they should be.
Our best model seems to be the one with CountVectorizer, so we will make our submission with that model.


Final prediction and submission

We have our model trained, with a somehow good accuracy. We will now train the model with the entire dataset, in order to show most of the data we have, and then we'll make the predictions wih the test dataset.

Predict the values
Generate Submission File.
