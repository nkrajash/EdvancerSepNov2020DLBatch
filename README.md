# EdvancerSepNov2020DLBatch
This is  Edvancer Certified Deep Learning Project 3: Spam filter for Quora questions

Problem statement:
Download data from here : https://www.dropbox.com/sh/kpf9z73woodfssv/AAAw1_JIzpuVvwteJCma0xMla?dl=0

Goal : Build a model for identifying if a question on Quora is spam 
Suggested Guidelines : 
1. To bring down dimensions of your model you can use glove embedding shared with you ( in the data )
2. Here is how you can use pertained embeddings : https://blog.keras.io/using-pre-trained-word-embeddings-in-a-keras-model.html
3. You'll have to Create and maintain your own train/validation splits for the full data shared with you 
4. Your solution needs to be uploaded to GitHub repo of your team.

My Solution:
1).Initially done the data preprocessing functionalities using data_preprocessing function like:
A.Data cleaning using regex
B.Lowercase translation
C.Tokenization
D.Stop words removal
E.Lemmatization
F.Joining the  words in preprocessed questions
2).Split the data set shared into trainig and validation data.
3).Used the following models and compared the F1- scores and accuracy:
  Model 1: Using Bag of Words (CountVectorizer)
    Validation accuracy:  0.9270640598003762
    Validation f1_score:  0.5412606943931684
  Model 2: TFIDF(Term Frequency Inverse Document Frequency)
    Validation accuracy:  0.9379461357656372
    Validation f1_score:  0.5113643214565623
  Model 3: Hashing Vectorizer 
    Validation accuracy:  0.8969163197962418
    Validation f1_score:  0.26971614536250227
4).With necessary preprocessing steps, first train a Bidirectional GRU model. 
5).Then without using any pre-trained word embeddings for this Bidirectional GRU model, 
the best threshold for F1 score was found to be 0.25 with score of 0.6400573433432678.
6).Now repeated step 4 and then train a Bidirectional GRU model with "Glove Embeddings",
the best threshold for F1 score was found to be 0.38 with score of 0.6723705617762464.
7).Repeated step 4 and then train a Bidirectional GRU model with  "Wiki News FastText Embeddings",
the best threshold for F1 score was found to be 0.32 with score of 0.6638568959154738.
8).The final blend was with 0.70*(predicted values of glove embedding) + 0.30*(predicted values of wikiNews Fast Text embedding),
the best threshold for F1 score was found to be 0.37 with score of 0.6747581286232235.
