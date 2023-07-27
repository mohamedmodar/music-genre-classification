# music-genre-classification

Getting the data ready

- Extracting all the genres we have in the dataset.
- Exploring the music files and its characteristics.
- ![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/bc901441-4c4f-4823-b31d-dd024219ba3f)

- Reading the dataset we have (features_3_sec.csv)
- Splitting the dataset into training and testing datasets. We will eventually
- 
have (X_train, X_test, y_train, y_test). We will then feed the model the
(X_train and y_train) datasets to train with. When the model is ready, we
input the (X_test) and compare the results with the (y_test) to see how
much the model can predict based on data he has never seen before.
- Scaling (X_train and X_test) to have all features range from 0 to 1. This
way we will have a better and faster model.
- Change the shape of (y_train and y_test).

-![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/636cea6e-e6ad-444e-a1f2-7079f298a59d)


Baseline model (Neural Network)

- As a baseline model, we used a neural network model.
- The model pramaters were (epochs_num = 20, batch_size = 5)
- After runing the model, we test it.
- The model outputs an array that has the size of the number of geners.
Each index stands for how much of each genre the song is. We take the
highest index.
- We got an accuracy of 64%.
Comparison of predict and real genre:

- ![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/e16ca163-7e7b-4cd7-a4db-e3405ab159fb)
- 
- - Confusion matrix:
  - 
![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/1679f907-f3e0-4899-9872-08e06541de8d)

KNN model

- As our main model, we used a KNN model.
- This time we used the cross validation technique to have the highest
accuracy we can reach.
- We first scaled down the (inputs) from the csv.
- We ran a 5-fold cross validation.
- At each fold, we calculated the accuracy of how much the model dealt
with the test data.
- The accuracy we had was up to 88%.
- 
- Comparison of predict and real genre:

- ![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/7d60b510-9229-4f4d-accd-709d0b5c9ade)
- 
- Confusion matrix:

![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/451de903-2c7d-4715-9d88-cbc1198ec27a)

Random Forest model

- We used a random forest model to have another opinion other than the
neural network.
- We ran a 5-fold cross validation.
- At each fold, we calculated the accuracy of how much the model dealt
with the test data.
- We also had an accuracy up to 88%.

- Comparison of predict and real genre:
- 
- ![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/2004e073-f63a-4b02-bc33-a100551efc22)

- - Confusion matrix:


- ![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/3ee6ba72-e680-4d2f-9eea-7e516ea72661)


Testing

![image](https://github.com/mohamedmodar/music-genre-classification/assets/120323472/be0926a3-8838-4b83-a7d0-153c7250b312)


- We ask the user to choose the index of a song from the csv.
- We then scale down the selected song features.
- We output the song’s genre before predicting.
- Then we input the selected song features to the NN, KNN and RF models.
- Then we output the number of models that got the genre right.
- For example: when choosing the 234th song, two of the models got it
right
