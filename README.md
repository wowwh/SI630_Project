# SI630_Project

## Abstract
Story understanding has long been a focus innatural  language  processing. In this project,we are going to learn a lot of five-sentence stories and try to predict the correct ending sentence for a four-sentence story, from two provided choices.


## Dataset
Our data are mainly from the Story Cloze Testand  ROCStories  Corpora  in  2016.The training set we will use is the ROC storycorpus called ROCStorieswinter2016.csv, includ-ing 98159 distinct stories.The test set has 1,871 different stories out of theother two datasets.


## Method

### 1 Doc2vec
We use dbow to train our doc2vet model so as to represent each sentence as a vector.

### Cosine
Our baseline is to use cosine similarity to directly measure the distance between two given choices with the beginning four sentences.


### 2 Logistic
We train a logistic regression model to measure whether a ending is true or false. We have two different ways of input. The first is use the full five sentences, and the second is use only the fourth sentence and the last one.


### 3 logistic2input
In this method, instead treating the story as a full sentence, while considering the input of the logistic model, the vecter of the first four(or one) sentences are concatenated with the last one. In other words, the dimension is doulbled.


### 4 Lstm
Lstm Model. Generate a endding and check which given choice is more close to it by cosine similarity.
