Adult Income Classification 

Problem & Dataset:
The project predicts whether a person's annual income is <=50K or >50K using the Adult Income dataset. It contains demographic, education, employment, and financial features such as age, workclass, occupation, education, marital status, capital gain/loss, and working hours.

Data Loading & EDA:
The dataset was loaded using Pandas and examined using head(), shape, info(), describe(), data types, missing values, and duplicates. EDA included class distribution, age distribution, occupation vs. income, education vs. income, and working-hours analysis using appropriate plots.

Data Cleaning:
Unnecessary columns were removed, duplicate records were handled, extra spaces were removed, and `?` values were treated as missing values. Missing numerical and categorical values were handled using appropriate imputation techniques. Numerical outliers were inspected rather than automatically removed because some extreme values can be valid.

Feature Engineering:
A total-capital feature was created from capital gain and capital loss. An `age-group` feature was also created. The education column was removed because `educational-num` provides a numerical representation of education level.

Vectorization & Scaling:
Categorical features were converted into numerical form using One-Hot Encoding. Numerical features were standardized using StandardScaler. Both were implemented through a preprocessing pipeline.

Model Training:
Three classification models were trained and compared: Logistic Regression, Decision Tree, and Random Forest.

Validation & Testing:
The data was divided into 80% training and 20% testing using stratified splitting. Five-fold cross-validation was also performed. Models were evaluated using Accuracy, Precision, Recall, F1 Score, and ROC-AUC. A confusion matrix and ROC curve were generated for the final model.

Model Saving & Prototype:
The complete trained pipeline was saved as adult_income_classifier.pkl. A Gradio GUI was created where users can enter personal and employment information and receive an income prediction with probabilities.

Key Findings & Conclusion:
EDA helped identify patterns between demographic/employment features and income. Model comparison showed differences in classification performance across algorithms. The project demonstrates a complete classification workflow from data loading and EDA to preprocessing, feature engineering, model training, evaluation, saving, and a working GUI prototype.
