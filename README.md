# Product_recommendation_media

#### The task was to build a binary classification algorithm that will give the liklihood of whether a particular customer will up-sell/cross-sell to additional products. 
The output of the model will be a probabilistic score which will indicate how likely a customer going to up-sell/cross-sell to additional products. 

#### --------------------------------------------------------------------------------------------------

### Modeling Approaches: 
#### For our purpose, I have trained the data on 3 models - First being logistic regression (baseline model) with and without upsampling using SMOTE.  
Then based on the results obtained, I decided to proceed with upsampled data for the rest of the process. 
Next, I tried Random forest an ensemble model that works by combining the performance of multiple weak learners by performing a majority voting of each these weak learner for classification task (Bagging algorithm - reduce variance). 
I have also performed hyper parameter tuning (Cross validation with Random search) on it by traning the random forest classifier with best parameters. 
Lastly, I have trained a XG Boost classifier which is a boosting algorithm - reduce bias which traines multiple classifiers in sequential manner and tries to improve performance based on the errors made by the previous learners.

#### --------------------------------------------------------------------------------------------------

### Model Evaluation:
#### For model evaluation, since the given dataset in imbalanced, we will use F-1 and Recall as our evaluation metrics. 
Recall is important because, in our specific use case, the cost of False Negative is more than the cost of False Positives i.e if our model wrongly classifies a potential customer who is more likely to up-sell/cross-sell , then it will hurt the business more than wrongly classifying a less potential customer. 
Furthermore, since the dataset is imbalanced, we will need to check the caliberation curve to indentify which model's predicted probabilities are more close to the actual probabilities.

#### --------------------------------------------------------------------------------------------------


### Recommendations:
#### Using the modeling approaches discussed below, the concerned media organisation can do three following things to drive its business - 

#### 1. CoE can identify specific key features from the data that play a crucial role in the decisions process of a customer up-sell/Cross-sell to additional products. Using this, CoE can focus on those features and work towards improving them. 

#### 2. For customers that are less likely to up-sell/cross-sell, CoE can send marketing campaigns to ensure less engaged customers are continuously using their products and devise strategies to up-sell/cross-sell products to these customers.

#### 3. For customers that are more likely to up-sell/cross-sell, Comcast can work on imporving the customer experience for this segment of customers by providing additional benefits like promotional discounts.
