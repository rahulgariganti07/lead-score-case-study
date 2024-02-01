# lead-score-case-study
# Problem Statement:
X Education is an online education company that sells courses to industry professionals. The company has a high lead generation rate, but only 30% of leads convert into paying customers. The CEO wants to develop a model and strategy to increase the lead conversion rate.

The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses fill up a form for the course, or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not.

Data
You have been provided with a lead dataset from the past with around 9000 data points. This dataset consists of various attributes such as Lead Source, Total Time Spent on the Website, Total Visits, Last Activity, etc. which may or may not be useful in ultimately deciding whether a lead will be converted or not. The target variable, in this case, is the column ‘Converted’ which tells whether a past lead was converted or not wherein 1 means it was converted and 0 means it wasn’t converted.

Steps for solving the problem:
Loading and understanding Data with description.
EDA
Data Preprocessing
Numerical Columns = We checked the missing values, Outliers
Categorical Columns = We checked missing values, What labels are present in each column and counts?
Data Visualization
Univariate Analysis – Explore each variable in the dataset.
Bivariate Analysis – Explore each variable with the Target variable.
Feature Engineering
Dummy variables created
Imputed Missing value with others. To avoid information loss, we did not drop the missing rows.
Dropped unnecessary columns.
Correlation check using the heat map, we check the correlation between independent columns to independent columns and independent columns to dependent columns. Also, we dropped the columns if the correction was too high, to avoid the multicollinearity.
Train test Split: Split the data with an 80-20 ratio. 80% training set and 20% test set.
Feature Scaling : Multiple columns are in different scales, so to normalize the range of features we used min-max scaling.
Feature Section : After the feature engineering, 68 independent variables were created and all 68 features are not important so we must select important features for model building. For selecting import features we used “rfe” and “vif” techniques.
Model Training : Using Logistic regression, we train our model with the most important features. We used 21 features for building the model.
Model Evaluation : We evaluated our model using a confusion matrix and focused on recall. We obtained a cutoff value of 0.3, which resulted in a recall of 92%, a precision of 85%, an F1 score of 89%, and an accuracy of 90% on the test data. The high recall value indicates that our model is good at identifying positive leads, even if it is less precise.
Conclusion:
Our model has achieved a recall of 92% on the test dataset, which means that it correctly predicts 92% of the positive leads. This meets the CEO's expectation of a lead conversion rate of around 80%.

We should focus on the following customer segments for lead conversion:

Working professionals
Customers who spend more time on the X Education website
Customers who visit the website regularly and have the highest page views per visit
Customers who have responded to previous emails
We should not focus on the following customer segments:

Customers who are interested in other courses
Students
By focusing on the right customer segments, we can further improve our lead conversion rate and achieve the CEO's goal of increasing revenue from online courses.
