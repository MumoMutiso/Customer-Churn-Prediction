Churn Rate Prediction
-------------------------------------------------------------
![image](https://github.com/MumoMutiso/Telco-Customer-Churn/assets/160124710/0a0a9cae-e73a-4027-99ac-aeac3b0b8a4c)

Technologies Used

- Power BI

- Python
- Streamlit
- Pandas
- Plotly
- Scikit-learn


--------------------------------------------------------------------------------------------------------------

About the Project
The churn rate is a metric that shows us the total percentage of clients who discontinue their subscriptions within a certain period.

Understandably, a high churn rate could affect a company's profitablity and also impact growth, so it's important to keep track of a company's churn rate and try to identify patterns among clients who discontinue their subscripitons in order to develop strategies to reach these clients with a better service, bonuses or any other incentive to keep them as clients for a long period of time.

In this project, I did an exploratory data analysis on a Telco dataset to find what the clients who left the company have in common and then I developed a machine learning model for churn prediction.

Column names and description
-------------------------------------------------------------------------------------------------------------


The data for this project is in differnt files and will be loaded into the notebook. The following describes the columns present in the data.

Gender -- Whether the customer is a male or a female

SeniorCitizen -- Whether a customer is a senior citizen or not

Partner -- Whether the customer has a partner or not (Yes, No)

Dependents -- Whether the customer has dependents or not (Yes, No)

Tenure -- Number of months the customer has stayed with the company

Phone Service -- Whether the customer has a phone service or not (Yes, No)

MultipleLines -- Whether the customer has multiple lines or not

InternetService -- Customer's internet service provider (DSL, Fiber Optic, No)

OnlineSecurity -- Whether the customer has online security or not (Yes, No, No Internet)

OnlineBackup -- Whether the customer has online backup or not (Yes, No, No Internet)

DeviceProtection -- Whether the customer has device protection or not (Yes, No, No internet service)

TechSupport -- Whether the customer has tech support or not (Yes, No, No internet)

StreamingTV -- Whether the customer has streaming TV or not (Yes, No, No internet service)

StreamingMovies -- Whether the customer has streaming movies or not (Yes, No, No Internet service)

Contract -- The contract term of the customer (Month-to-Month, One year, Two year)

PaperlessBilling -- Whether the customer has paperless billing or not (Yes, No)

Payment Method -- The customer's payment method (Electronic check, mailed check, Bank transfer(automatic), Credit card(automatic))

MonthlyCharges -- The amount charged to the customer monthly

TotalCharges -- The total amount charged to the customer

Churn -- Whether the customer churned or not (Yes or No)


Hypothesis
-------------------------------------------------------------------------------------------------------------
Hypothesis 1
Null Hypothesis (Ho): There is no significant difference in churn rates between customers with shorter and longer tenure.

Alternative Hypothesis (Ha): There is a significant difference in churn rates between customers with shorter and longer tenure.

Hypothesis 2 
Null Hypothesis (Ho): There is no significant difference in churn rates between customers with higher and lower monthly charge.

Alternative Hypothesis (Ha): There is a significant difference in churn rates between customers with higher and lower monthly charge.

Questions
------------------------------------------------------------------------------------------------
What is the average tenure of customers who churned compared to those who stayed?

Do customers with partners or dependents have a lower churn rate?

How does the presence of multiple lines affect customer churn?

Is there a correlation between the contract term (Contract) and customer churn?

What are the common payment methods (Payment Method) among customers who churned?

How does the availability of tech-related services (e.g., OnlineSecurity, TechSupport) impact churn rates?

What percentage of customers who churned had streaming services (StreamingTV, StreamingMovies)?

Is there a difference in churn rates between senior citizens and non-senior citizens?

How does the total amount charged to customers (TotalCharges) correlate with churn behavior?

How does the contract affect churn rates?



Datatypes
------------------------------------------------------------------------------------------
Dataframe and Datatypes Understanding
The dataset was loaded into a Pandas DataFrame using the pd.read_csv function. The dataset contained 20 columns/features and 5043 rows.


This output of the dataframe.info() revealed that the 20 columns in with their corresponding data types had no missing values (since all columns have 5043 non-null values), but the TotalCharges column was in object instead of float64. This suggests that there may be some non-numeric values in this column that need to be cleaned.



Customer Profile Overview
--------------------------------------------------------------------------------------------------------------------------------------

👤 Customer ID: Unique identifier facilitating personalized engagement and loyalty programs for enhanced customer experience.

🔄 Churn Index: Dynamic metric gauging the propensity of customers to churn, enabling proactive retention measures and revenue protection.

💰 Total Charge: Financial indicator reflecting customer value and profitability, guiding pricing strategies and targeted promotions.

🛡️ Risk Level: Visualize churn risk levels to prioritize retention efforts and allocate resources effectively for maximum impact.

📝 Personal Details: Dive into demographic insights such as age, gender, and location to tailor offerings and communication channels to specific customer segments.

📄 Contract Details: Understand contract specifics like type, duration, and terms to optimize renewal strategies and minimize churn risk.

💼 Additional Insights: Explore service usage patterns, feedback, and engagement metrics to craft personalized retention strategies and foster long-term loyalty.


Summary of findings from the analysis
------------------------------------------------------------------------------------------
Below are some findings drawn from the jupyter notebook for your kind attention

Data handling packages like pandas and numpy were used
Packages for feacture processing, machine learning and hyperparemeter tuning were also used to acheive the object of the analysis
Other packages such as tabulate, os and warnings were also used.
Regarding the hypothesis,
There is a significant difference in churn rates between customers with shorter and longer tenure.
There is a significant difference in churn rates between customers with higher and lower monthly charges.
The best performing model was Logistic Regression.


Limitations
----------------------------------------------
Limitation 1 : In this dataset, we can only see one type of each variables instead of real world situation of changing different options as time passes, e.g., in real world, people might want to try streaming service, but they might change their mind to leave the service next month.

Limitation 2 : We cannot only see these variables as whole factors to understand the exact reasons why customers left because they might leave for better price offered by competitors or the bad economy in certain time, etc. We also cannot see the time they leaked, so it's hard to infer those external situations.

Conclusion
-------------------------------------
Churn analysis represents a strategic initiative aimed at leveraging data-driven insights to mitigate customer attrition and foster long-term loyalty. By harnessing the power of classification models, the company endeavors to enhance customer retention efforts, drive sustainable revenue growth, and maintain a competitive edge in the dynamic marketplace.
