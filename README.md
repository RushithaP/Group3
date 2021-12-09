# Group3
## Domain: Banking & Finance

## Project Title
Classifying Loan approval status using Machine Learning Algorithms

## Group Members
* Jinye Li (jli74@uncc.edu)
* Rushitha Reddy Palgutta (rpalgutt@uncc.edu)
* Pratheeka Thummala (pthummal@uncc.edu)
* We are a group of Computer Science graduate students at the University of North Carolina at Charlotte

## Installation
* Anaconda 4.5.12 Distribution
* Python 3.7
* Jupyter Notebook

## Introduction to Problem or Opportunity
The banking sector is a booming industry where it earns the majority of its profits from interest on the loan they assign. Computers nowadays are intelligent enough to perform nearly all human tasks. In light of this, we are currently training a model to know if a customer is likely to get loan approval or not. For this, we have gathered data from websites like Google, Kaggle and UCI merged them into one depending on the features that are relevant for us to work on. We will use different classification algorithms employing techniques like standardization, feature extraction, Principal Component Analysis (PCA), and modeling  to arrive at our solution and identify which one (algorithm) gives us the maximum accuracy
### Targeted Audience: 
This will be beneficial for anyone planning to provide financial services, as we aim to automate the process of determining and predicting a customer's eligibility in advance. As a result, the level of risk that the investor will face will be reduced to some extent in this domain.

## Research Question
The outcome of the project is whether or not the loan is sanctioned after considering all the records of a particular person. Loan sanction depends on income, age, qualification, the purpose of taking a loan. Since we are using other variables to describe the outcome i.e., with the help of income we are predicting if we get the loan or not. As a result, predictive analysis is being performed here.
* Extract features/variables which will decide if the loan can be sanctioned or not, other than the Property_Area?
* Which classifier or algorithm will provide the maximum accuracy amongst all.

## Data Resources
https://www.kaggle.com/anmolkumar/analytics-vidhya-loan-prediction/code <br>
https://datasetsearch.research.google.com/search?query=Loan%20Prediction%20Problem%20Dataset&docid=L2cvMTFqbl9iend6ag%3D%3D <br>
https://www.kaggle.com/itssuru/loan-data <br>
This dataset contains over 1,000 records including variables like Loan_ID,	Gender,	Married	Dependents,	Education,	Self_Employed,	ApplicantIncome,	CoapplicantIncome, LoanAmount,	Loan_Amount_Term,	Credit_History, Property_Area	and Loan_Status. Here, "Loan_Status" is the target variable. We are trying to merge all the above data into one data frame and then perform training and testing to predict the target variable. 

## CRISP-DM (Cross Industry Standard Process for Data Mining) Process Model
Regardless of the domain, this methodology offers a unique approach to representing the stages of development of any data science project and has been proven to be efficient. It has a six-step cycle that goes as follows:
### 1. Business Understanding
* Numerous banks and financial organizations continue to approve loans through a rigorous verification and validation process, but there is no guarantee that the chosen candidate is the most deserving of all applicants. We want to facilitate selecting qualified applicants as quickly, simply, and easily as possible. 
#### In our application:  
* No stakeholders will be able to influence the outcome because the entire prediction process will be completed in private. Outcomes in relation to specific loan Ids can be sent to various bank divisions so that appropriate action can be taken on the application.
* We classify the weight of each feature involved in loan processing through our application, and the same characteristics are processed on new test data concerning their associated weight.

### 2. Data Understanding and EDA
#### Gathering data
  * We obtained data from Kaggle that was relevant to our study, verified it, and processed it. The data file is being uploaded to the list of files above. 
#### Describing data
  * We loaded the data into a data frame to do our operations as it is stored in CSV (Comma Separated Values) format. The parameters are as follows.
    * Loan_ID: Unique Loan ID
    * Gender: Male/ Female
    * Married: Applicant married (Y/N)
    * Dependents: Number of dependents
    * Education: Applicant Education (Graduate/ Undergraduate)
    * Self-employed: Self employed (Y/N)
    * ApplicantIncome: Applicant income
    * CoapplicantIncome: Co applicant income
    * LoanAmount: Loan amount in thousands of dollars
    * Loan_Amount_Term: Term of a loan in months
    * Credit History: credit history meets guidelines yes or no    
    * Property Area: Urban/ Semi Urban/ Rural
    * Loan Status: Loan approved (Y/N) this is the target variable
#### Exploring data
  * We have conducted the preliminary analysis of data patterns to examine the data, make assumptions and perform operations by visualizing the statistics, graphs, and relations in the data. For visualizations, we utilized seaborn and matplotlib, and for data manipulation, we used pandas. The distribution is skewed, and there are several outliers and also found missing values in 'Gender', 'Married', 'Dependents', 'Self-employed', 'LoanAmount', 'Loan_Amount_Term', 'Credit History', 'Loan Status'. Discovered that 'Credit History' had a greater impact on the output variable by looking for correlations in the data. 
### 3. Data Preparation
* Handled the missing values in the data by filling the numerical missing values with the mean and for categorical values, we filled them with the mode. Further, we have addressed the outliers. One approach would be to just eliminate them; alternatively, we may log convert them to nullify their influence, which is what we did here. Through the boxplot, we see that people with more education have a greater income. Similarly, we comprehended the relativity of other features in relation to our target variable.
### 4. Modeling (Machine Learning)
* We have done implementing Predictive Machine Learning algorithms like Logistic Regression, Random Forest Classifier, Decision Tree Classifier, and KNN
To build our models, we have used 'sklearn' library and coverted all of the categorical variables to integers. Writing a function that inputs a model, fits it, and measures the accuracy, which entails using the model on a train set and measuring the inaccuracy on the same set
### 5. Evaluation 
* We have used evaluation methods such as the confusion matrix, precision, recall, f1-score, support, and model scores to decide the predictive models. Also, evaluated if our model is overfitted by using the cross-validation score as a metric. 
### 6. Conclusion
To sum up our work, the visualizations we built from our unique client data enable users to gain significant insights and make faster decisions. Prior to the modeling phase, operations such as data cleaning and preprocessing were done. We were able to handle missing values and outliers, as well as eliminate features that were less correlated with the target variable by conducting the dimensionality reduction as a part of data preprocessing. Many columns in the training and testing dataset were not the same. So we combine them and then work on them to handle the imbalanced data. 

We have implemented machine learning classifiers like decision tree classifier, random forest classifier, and KNN Classifier. Amongst which Decision tree classifier was proven to have more accuracy. 
Despite the challenges faced to find the classifier that gives the most accurate results, the model thus predicts if a customer is eligible for loan approval or not.
## Future Work
* Verifying if the person has given all the correct information to the bank.
* Since no classifier provides 100 percent accuracy, identify the amount of risk that the bank will incur if a loan is approved is crucial.
* If provided with more in-depth details like credit and debit history the project can be elevated to another level of data exploration.


