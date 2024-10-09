# Final_Capstone_Project
## Cardiovascular Disease Detection Capstone Project

### Mahalakshmi Ganesan

### Business Rationale
#### Cardiovascular disease is a term that encompasses a myriad of diseases that impact the heart and its blood vessels. These diseases are extremely detrimental to a patient's health and their longevity. Cardiovascular disease impact over 10 million patients every year. It is also the leading cause of death both nationally and globally. Given its severe nature and widespread impact, this disease is one, that if caught early, can save millions of lives and provide a better quality of life to millions.

### Research Question
#### There are many contributing factors to Cardiovascular Disease. These include genetics, lifestyle choices, diet and many more. Based on the specific Demographics, Vital Signs, and Laboratory Factors, we are working to determine which are the highest contributing factors in detecting the Presence or Absence of Cardiovascular Disease.

### Data Sources
#### This dataset was obtained from kaggle.com from the following link [Cardiovascular Disease Dataset](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset).
#### The dataset originally had 70,000 observations, 11 feature variables and 1 target variable. The feature variables are Age, Gender, Height, Weight, Systolic Blood Pressure, Diastolic Blood Pressure, Cholesterol, Glucose, Smoking, Alcohol Intake, and Physical Activity.
#### The dataset had no null values. There are 5 numeric features in this dataset and there are 6 other categorical variables that had been assigned numeric values for their categorical values. The numeric variables are Age (in days), Height (in cm), Weight (in kg), Systolic Blood Pressure and Diastolic Blood Pressure. The categorical features are Gender (1=women and 2=men), Cholesterol (1=Normal, 2=Above Normal, 3=Well Above Normal), Glucose (1=Normal, 2=Above Normal, 3=Well Above Normal), Smoking (1=Yes, 2=No), Alcohol Intake (1=Yes, 2=No), and Physical Activity (1=Yes, 2=No).
#### The target variable is Cardio and this is a binary variable in which 1=Presence of Cardiovascular Disease and 0=Absence of Cardiovascular Disease.

### Methodology
#### Upon analysis of the data, there were values in Height, Weight, Systolic Blood Pressure and Diastolic Blood Pressure that were extreme values that would not biologically be possible. Based on this determination, the dataset was subset to only include subjects whose Heights are between 140cm and 200cm, Weight is above 55kg, Systolic Blood Pressure is between 90mmHg to 180mmHg and Diastolic Blood Pressure is between 60mmHg and 120mmHg. This resulted in a dataset 64,840 observations.
#### Additionally, Age was also converted from being measured in Days to being measured in Years.
#### The data was then split into a training dataset and a test dataset based on the X variables and the y variable. 
#### After the training and test datasets were generated for the X variables and y variable, a Selector criterion was assigned to include data types that include both numeric data types and object data types. A transformer criterion was assigned to the model analysis in which data is Standard Scaled. Finally, an extractor criterion was assigned with Logistic Regression in which L1 Penalty was used and a Liblinear Solver.
#### Upon assigning the 3 criteria, a Model Pipeline was run and fitted with the training datasets of the X variables and the y variable.
#### A model was outputted in which the 11 features were listed in descending order of importance to the prediction of the Presence or Absence of Cardiovascular Disease.
#### Finally, with the target variable being balanced, accuracy score and precision score was used as an appropriate metric for evaluating the model.

### Results
#### During the exploratory analysis of the dataset, it was noted that the target variable is equally balanced within the subset dataset.
![Target_Proportions](https://github.com/maha0491/Final_Capstone_Project/blob/808d3140df591a1360d6741bdc7094b6e5216e90/Images/Target_Proportions.png)
#### Upon running the Logistic Regression model, it was determined that the top 4 feature variables with the most impact in determining the presence or absence of Cardiovascular Disease are Systolic Blood Pressure, Cholesterol, Age and Weight. 
#### The distributions of the 4 key factors are as follows:
![Systolic Blood Pressure_Distribution](https://github.com/maha0491/Final_Capstone_Project/blob/808d3140df591a1360d6741bdc7094b6e5216e90/Images/SysBP_Distribution.png)

![Cholesterol_Proportions](https://github.com/maha0491/Final_Capstone_Project/blob/808d3140df591a1360d6741bdc7094b6e5216e90/Images/Cholesterol_Proportions.png)

![Age_Distribution](https://github.com/maha0491/Final_Capstone_Project/blob/808d3140df591a1360d6741bdc7094b6e5216e90/Images/Age_Distribution.png)

![Weight_Distribution](https://github.com/maha0491/Final_Capstone_Project/blob/808d3140df591a1360d6741bdc7094b6e5216e90/Images/Weight_Distribution.png)
#### In addition, due to the target variable being balanced,  accuracy score and precision score are 0.73 and 0.76 respectively.

### Next steps
#### To better improve the model and to derive a more accurate model when determining Cardiovascular Disease, an increase in the quantity and quality of the data that is provided is vital. In addition, many factors also aid in a patient having such disease. With the inclusion of more factors that potentially would impact the presence or absence of the disease, a better and more accurate model may be derived. 
#### Based on the derived features from the Logistic Regression, the proposed next steps would be to recommend patients with higher Systolic Blood Pressure, who are Well Above Normal in their Cholesterol, older in Age and heavier in Weight to begin routinely getting tested for Cardiovascular Disease. By beginning testing during the early signs of these 4 features, doctors and patients will be able to detect Cardiovascular Disease earlier and be able to treat or manage the disease. This will improve their quality of life and their longevity by magnitudes. 

### Outline of project

- [Cardiovascular_Disease_Exploratory_Data_Analysis.ipynb]( https://github.com/maha0491/Final_Capstone_Project/blob/5174ec31a146966b0405db9897ad3104a0493593/Cardiovascular_Disease_Exploratory_Data_Analysis.ipynb)
- [Cardiovascular_Disease_Logistic_Analysis.ipynb]( https://github.com/maha0491/Final_Capstone_Project/blob/5174ec31a146966b0405db9897ad3104a0493593/Cardiovascular_Disease_Logistic_Analysis.ipynb)

#### Contact and Further Information
##### Mahalakshmi Ganesan
##### Email: maha0491@gmail.com
