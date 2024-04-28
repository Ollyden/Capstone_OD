# TITLE OF PROJECT
Stroke prediction utilising patient data


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
The WHO states that strokes are the 2nd leading cause of death globally. This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases and whether they smoke.

## DATA
1) id: unique identifier
2) gender: "Male", "Female" or "Other"
3) age: age of the patient
4) hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5) heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6) ever_married: "No" or "Yes"
7) work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8) Residence_type: "Rural" or "Urban"
9) avg_glucose_level: average glucose level in blood
10) bmi: body mass index
11) smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12) stroke: 1 if the patient had a stroke or 0 if not
*Note: "Unknown" in smoking_status means that the information is unavailable for this patient

This data was downloaded on Kaggle -> see the link https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset/data

## MODEL 
For this capstone project I use a random forest algorithm, with smote rebalancing. After testing a couple of different algorithms, random forest returned the highest accuracy. 

## HYPERPARAMETER OPTIMSATION
It was noted that a train/test split ratio of 70/30 performed best in the random forest model. 

In the smote rebalancing, a sampling_strategy parameter of 0.4 achieved the highest accuracy. 

In the random forest model, n_estimators=100 worked out to be a good balance of decision trees v.s. what could be high computational cost. After trialling a few different values for max_depth, it was clear smaller values (i.e. limiting the tree depth) reduced the accuracy.


## RESULTS
We ended with a result of 95% accuracy, utilising a random forest algorithm. The key takeaway was that this model proved the importance of rebalancing the data using Smote rebalancing, as without this the algorithm failed to predict any cases of strokes. 

It was also noted that a train/test split ratio of 70/30 performed best in the random forest model. 

The smote rebalancing was performed at a 40% rebalance rate, which achieved a result that had a similar ratio of stroke / no stroke as the original dataset.

An SVM algorithm was also trialled, but this performed more poorly than the random forst algorithm, despite trialling multiple different kernels. 

