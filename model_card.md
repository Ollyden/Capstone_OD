# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

**Input:** The inputs of the model include various features related to individuals' demographic and health-related information. These features include age, gender, hypertension, heart disease, average glucose level, BMI, residence type, work type, and smoking status.

**Output:** The output of the model is a binary prediction indicating whether an individual is likely to have a stroke or not (1 for stroke, 0 for no stroke).

**Model Architecture:** The model architecture used is a Random Forest classifier, with smote rebalancing. 

## Performance
The performance of the model was measured using accuracy and a confusion matrix. The accuracy of the model was high (0.955), but special consideration had to be made to the confusion matrix, as initially (without smote rebalancing) the model failed to predict any cases of strokes. The rebalancing was necessary for the model to accuractly identify cases of stroke. 

## Limitations
Random forest algorithms could be considered black box algorithms, where the decision making for classes isn't clear. This algorithm is also heavily reliant on good quality input data. 

## Trade-offs
Given that there is likely to be a huge dataset in reality, there could be some significant computational costs associated with training a random forest algorithm. It could also be the case that the model becomes prone to overfitting and may not be accurate in real life - some monitoring would need to be done to check for this in the initial launch phases. 
