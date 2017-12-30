# Classify yelp reviews
Classify Yelp round-10 reviews/comments


# Basic Information:

In this project, I classify Yelp round-10 review datasets. The reviews contain a lot of metadata that can be mined and used to infer meaning, business attributes, and sentiment. For simplicity, I classify the review comments into two class: either as positive or negative. Reviews that have star higher than three are regarded as positive while the reviews with star less than or equal to 3 are negative. Therefore, the problem is a supervised learning. To build and train the model, I first tokenize the text and convert them to sequences. Each review comment is limited to 50 words. As a result, short texts less than 50 words are padded with zeros, and long ones are truncated. After processing the review comments, I trained three model in three different ways: 

<li> Model-1: In this model, a neural network with LSTM and a single embedding layer were used. 
<li> Model-2: In Model-1, an extra 1D convolutional layer has been added on top of LSTM layer to reduce the training time.
<li> Model-3:  In this model, I use the same network architecture as Model-2, but use the pre-trained glove 100 dimension word embeddings as initial input.

Since there are about 1.6 million input comments, it takes a while to train the models. To reduce the training time step, I limit the training epoch to three. After three epochs,it is evident that Model-2 is better regarding both training time and validation accuracy.

# Codes and Libraies

All of the projects requires Python 2.7 or 3 I have Used python 3.0. The following Python libraries are also required:

<li> NumPy
<li> Pandas
<li> Matplotlib
<li> Scikit-learn
<li> Nltk
<li> Plotly
<li> Keras

# Word embeddings
<li> Glove
<li> word2vec

# Datasets are not included to this project due to size.

The Yelp dataset is a subset of our businesses, reviews, and user data for use in personal, educational, and academic purposes. Available in both JSON and SQL files, use it to teach students about databases, to learn NLP, or for sample production data while you learn how to make mobile apps.

# Contributors
Sabber Ahamed

# License
MIT