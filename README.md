# EdvancerSepNov2020DLBatch
This is  Edvancer Certified Deep Learning Project 2: Music Genre Identification

Download data from here :  https://www.dropbox.com/s/4jw31k5mlzcmgis/genres.tar.gz?dl=0

Goal : Given audio files for songs , identify which genre they fall in 
Suggested Guidelines : 

1. You'll have to prepare and maintain your own version of train and validation from the full data given 
2. Major challenge here is to create features from audio files which can then be passed to your choice of deep learning algorithm 
3. Your solution needs to be uploaded on GitHub repo of your team

My Solution:
Music_genre_classification_using_CNN.ipynb:

The steps followed here are:

1.Extracting music and features from the data set where each of 10 genres have 100 songs each.

2.Extracting the Spectrogram for every Audio (with visual representation of the spectrum of frequencies varying with time)

3.Extracting features from Spectrogram like:
* RMSE(Root Mean Squared Error)
* Mel-frequency cepstral coefficients (MFCC)(20 in number)
* Spectral Centroid
* spectral_bandwidth
* Zero Crossing Rate
* Chroma Frequencies
* Spectral Roll-off

4.Writing the data to a new csv file (called data.csv)

5.Analysing the Data in Pandas the respective features with the filename.

6.Encoding the labels and then apply Standard Scaler to the feature columns

7.Split the data as training and test data

8.Then we do classification using Keras and build our Network.Check the tentative performance using validation data from the training data set.

9.Then the prediction on the test data gave an accuracy score of 0.635.

10.Further improvements can be made by applying other models for the music genre classification.
