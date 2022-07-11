# XGBoost-model

model description
This is XGboost classifier built as part of Kaggle ML competition during ML course I have taken as part of my Msc. degree.

To classify the activity of TP53 protein into 3 classes we used XGboost classifier. Firstly, to clean the data, we preformed preprocessing that contain the following steps:

EDA

- Created concatenated data frame based on the trained and the test data given - we did so for increasing the statistical power of our pre-processing analysis.

-observed for each feature whether it contain null values

-Excluding highly correlated features( eliminating one of the features that correlated the other feature if the spearman correlation result is correlated in more than 90 %) to benefit the learning process.

-Removed low variance feature to effeiently affect the learning proccess.

-Standard transformation of the data, since it is highly recomended to transform the data when using XGBoost.

After the EDA was finished , the data was splitted for training and validation.I have tried using also deepchem splitting according to te chemical scaffold yet it didnt work well as random splitting

Random oversampling to balance the data was used. (since SMOTE method for oversampling isnt appropraite in this case as chemical copmounds need regulations to be generated.i.e not every bond is possible).

XGboost classifie was built .the model thenn were checked, if it overfitted, and then some of the parameters were changed to reduce overfitting.
