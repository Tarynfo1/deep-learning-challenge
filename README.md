# deep-learning-challenge
Using machine learning and neural networks to predict success in applicant funding in the non-profit sector.

<img width="1440" alt="fundraising" src="https://github.com/Tarynfo1/deep-learning-challenge/blob/93f19fb58d6f909f8219301b513a036b9659d861/Resources/Fundraising_imagejpg.jpg">


*** 
## Background
The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

***
## File structure
- __Code:__ Contains initial model and optimization model code
- __Resources:__ Contains image files for readme and h5 files
- __README.md:__ ReadMe file including instructions and _Report_

***
## Tools
- Pandas
- ScikitLearn
- TensorFlow
- h5
***
## Instructions<br>
_Step 1._ Using your knowledge of Pandas and the Scikit-Learn’s StandardScaler(), you’ll need to preprocess the dataset in order to compile, train, and evaluate the neural network model later in Step 2   

Read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:
    * What variable(s) are considered the target(s) for your model?
    * What variable(s) are considered the feature(s) for your model?

_Step 2._ Using your knowledge of TensorFlow, you’ll design a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. You’ll need to think about how many inputs there are before determining the number of neurons and layers in your model. Once you’ve completed that step, you’ll compile, train, and evaluate your binary classification model to calculate the model’s loss and accuracy.


_Step 3._ Optimize your model in order to achieve a target predictive accuracy higher than 75%. If you can't achieve an accuracy higher than 75%, you'll need to make at least three attempts to do so.
    
    
_Step 4._. Write a report on the performance of the deep learning model you created for AlphabetSoup



***
## Report <br>
***

### Overview

Tasked with creating an algorithm to predict if applicants for funding will be successful for the not-for-profit organisation, Alphabet Soup - features provided in the dataset were used to create binary classifiers that are capable of rpedicting whether applicants will be successful in their funding applications.

### Data Preprocessing

To start, data was cleansed to remove information that was not relevant, which was EIN and NAME, the remaining columns were to be the considered features of the model. For binning purposes, name was added back in the second test. The data was then split for training and testing set. The target variable used for the model is labeled 'IS_SUCCESSFUL" and has the value of 1 for yes and 0 for no. Thne, the APPLICATION data was analysed and the "CLASSIFICATION" value was used for binning. Several data points were used as a cut off to bin "rare" variables together with the new value of "Other" for the unique values. Categorical variables were encoded by get_dummies() after checking to see if the binning was successful.


#### Compiling, Training and Evaluation of the model

After applying the neural networks, there were 3 layers of each of the models. The number of hidden nodes depended on the number of features (see below).

<img width="360" alt="layers" src="https://github.com/Tarynfo1/deep-learning-challenge/blob/93f19fb58d6f909f8219301b513a036b9659d861/Resources/layers1.png"><br><br>

477 parameters were created by a three-layer training model, the first try show accuracy just above _73%_, sitting just under 75%:<br>
<img width="360" alt="results73" src="https://github.com/Tarynfo1/deep-learning-challenge/blob/93f19fb58d6f909f8219301b513a036b9659d861/Resources/Results73.png"><br><br>


### Summary

The optimisation performance included the NAME column included in the dataset and achieved an accuracy of _79%_ which is _4% over the target_ with 3298 parameters.<br>


<img width="360" alt="results79" src="https://github.com/Tarynfo1/deep-learning-challenge/blob/93f19fb58d6f909f8219301b513a036b9659d861/Resources/results79.png"><br><br>

### Recommendation
Given that multiple layers learn how to predict and classify information based on filtering inputs through layers, it is recommended to use them for deep learning models.
