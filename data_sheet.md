
## Motivation

Purpose: The dataset was created to develop a predictive model for identifying individuals at risk of stroke based on their demographic and health-related information.

Creators: It is not currently known who developed this dataset. It was downloaded from https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset/data

 
## Composition

- The instances in the dataset represent individuals with various demographic and health-related characteristics.
- There are 5110 records in this dataset.
- There was some missing bmi data, which was filled with the median value of bmi for that respective gender. 
- Yes, this data is healthcare related information, and as such is very sensitive. 

## Collection process

- It is unclear how the data was collected, but it may have been collected from medical records, surveys, or other sources of healthcare data.

- The timeframe and size of this sample set in relation to the full dataset is not known. 

## Preprocessing/cleaning/labelling

- Data preprocessing of this dataset was necessary:
  - To fill null values of bmi
  - To change categorical vairables into binary variables (either using           one-hot encoding or binary encoding)
  - to drop unecessary rows
  - To split the data into features & target
  - To bulk out the 'stroke' cases int he dataset (smote rebalancing)
 
## Uses

- Aside from detecting stroke risk in patients, this dataset could be used to   explore the relationship between various health factors and outcomes of       medical diagnosis. 
- Note that this data could contain biases, such as the under representation    of certain demographical groups, and as such lead to biased outcomes. 

## Distribution

- It is not clear how the data has been distributed, however it is likely to be subject to copywrite by the organisation that collected it.

## Maintenance

It is currently unknown who maintains this dataset. 

