# classification-challenge

<div align='center'>
    <img src='Spam_Filter.png' alt='Image of 2 spam emails and one regular email going through a classifier'/>
</div>

## Overview

* Classification is the method to predict discrete valued variables. A discrete variable has no middle, and its values cannot be divided. Data scientist use classificaiton to draw categorical conclusions about data (true-positive/true-negative)

Hypothesis: Random Forest Classifier will perform better due to the utilization of ensemble learning to randomnly sample data and create decision tree for smaller portions of data. By combining the smaller decision trees to create a stronger classifier, the Random Forest Model will have much better decision-making accuracy than the Logistic Regression Model.

## Methods

* Modeling Steps
    * Preprocess - cleaning the data by removing rows with missing values and splitting data into subsets for training and testing the model.
        * `StandardScaler` - scales data to have a mean of 0 and variance of 1.
        * `MinMaxScaler` - scales feature data to a minimum of 0 and a maximum of 1 (Not used for this spam detector model assignment)
    * Train - Use a large subset of labeled data to teach the model to recognized classification patterns.
    * Validate - use a small subset of labelled data to test how well the model is able to predict labels.
    * Predict - use model to predict labels for unclassified data.

* Logistic Regression is a statistial method for predicting binary outcomes from data.

* Random Forests Classifier is based on the principal of ensemble learning, combining more than one decision tree to create a forest of trees. This type of learning accumulates the predictions to make a final prediction.

## Landscape
* Classification can be used in the loan application process to determine whether the applicant owns a car or not. It can be used to classify the health of startups to gauge the risk associated with a bank loan. It can be used to filter spam messages out of email inboxes of classify customer reviews on social media as positive or negative. Classification can predict whether a customers will churn or not, and whether credit card transactions are fradulent or not.

## Business Advantage
* Classification models have greatly improved the ability for organizations to properly classify applicants, predict market decline, and classify fradulent transactions or suspicious activity.

* Some the advantages of the Random Forest Algorithm include minimizing overfitting given all weaker learners are trained on different pieces of data. Regarding large or nonlinear datasets, algorithm can handle thousands of input variables without variable deletion. It can also rank the importance of input variables in a natural way, and is less sensitive to outliers.

## Results

<div align='center'>
    <img src='images/Random_Forrest.png' alt='Nine trees representing a subset of data ramdonly sampled and the corresponding prediction'/>
</div>

* The Random Forest Model performed better than the Logistic Regression model based on the accuracy score which adheres to my predictions, however I was expecting a much larger disparity than .04 between the two models. My predictions were based on the Random Forest Model being capable of capturing complex, non-linear relationships between features by sampling different combinations and interactions of features which is integral to identifying spam. Spam detection datasets often contain intricate patterns a linear regression model may not be able to capture as effectively.

## Recommendations

* Compare the performance of Random Forest Model with another ensemble learning model like ExtraTrees to determine how the approach to randomness effects accuracy.

* Random Forests uses bootstrap sampling, meaning each tree is trained on a bootstrap sample (random sample with replacement) of the training data. At each split in the tree, a random subset of features is selected based on the Gini impurity or entropy, and the best split among thoese features is chosen.

* ExtraTrees uees the whole original sample rather than bootstrap samples to train each tree, and then creates each split in the tree randomnly for each feature.