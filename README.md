# Lead-Scoring-case-study
# Problem Statement
*An education company named X Education sells online courses to industry professionals. On any given day, many professionals who are interested in the courses land on their websites and browse for courses. 

The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%. 

Now, although X Education gets a lot of leads, its lead conversion rate is very poor. For example, if, say, they acquire 100 leads in a day, only about 30 of them are converted. To make this process more efficient, the company wishes to identify the most potential leads, also known as ‘Hot Leads’. If they successfully identify this set of leads, the lead conversion rate should go up as the sales team will now be focusing more on communicating with the potential leads rather than making calls to everyone.

# Steps in study
The following steps were undertaken to achieve the study's goals:

1.	Data Cleaning: The initial dataset was relatively clean, with only a few null values. The "option select" category was replaced with a null value since it didn't provide significant information. Some null values were transformed into "not given" to retain data. However, these "not given" values were subsequently removed when creating dummy variables. Additionally, the geographical data was categorized into "India," "Outside India," and "not given" to differentiate between locations.

2.	Exploratory Data Analysis (EDA): A preliminary EDA was conducted to assess the quality of the data. It was observed that certain elements in the categorical variables were irrelevant. On the other hand, the numeric values appeared to be sound, with no outliers detected.

3.	Dummy Variables: Dummy variables were created for the categorical variables, and the dummy variables containing "not given" elements were eliminated. The MinMaxScaler technique was applied to normalize the numeric values.

4.	Train-Test Split: The dataset was divided into 70% training data and 30% testing data.

5.	Model Building: The Recursive Feature Elimination (RFE) technique was employed to identify the top 15 relevant variables. The remaining variables were manually removed based on their Variance Inflation Factor (VIF) and p-values. Variables with VIF < 5 and p-values < 0.05 were retained.


6.	Model Evaluation: A confusion matrix was created to assess the model's performance. The Receiver Operating Characteristic (ROC) curve was used to determine the optimal cutoff value, resulting in an accuracy, sensitivity, and specificity of approximately 80% each.

7.	Prediction: Predictions were made on the test dataset using an optimal cutoff of 0.35, yielding an accuracy, sensitivity, and specificity of 81%.

8.	Precision-Recall: The Precision-Recall method was also employed to validate the results. A cutoff value of 0.41 was identified, resulting in a precision of approximately 73% and a recall of approximately 77% on the test dataset.

# Conclusion
*Based on the findings, X Education can greatly benefit from focusing on the identified variables to attract potential buyers, particularly industry professionals. By leveraging these insights, X Education has a high probability of successfully influencing potential buyers and encouraging them to enroll in their courses.
