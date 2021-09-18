## Salary Prediction Portfolio

### Problem Definition:

The purpose of this project is to make accurate salary predictions that are based on existing known salaries, so the company can recruit and retain top talent. This model will help the company for offering competitive pay to existing and future employees. 
Data transformation and machine learning will be used to create a model that will predict a salary when given job description category, contract type, and contract time:
The data for this model consists of a training dataset with the features listed below and their corresponding salaries. Twenty five percent of this training dataset was split into a test dataset with corresponding salaries so accuracy and error of the model can be determined. 

### The features in this data set are described as below:

**•	Job Code: Primary Key - unique identifier for each job posting**    
**•	Title: - The job posting title**    
**•	Job Description: Job level description**    
**•	Region: Job posting regional area**   
**•	Location: Job posting location**    
**•	ContractType: Contract Posting (e.g Part-time, Full-Time)**   
**•	ContractTime: Job Posting Time (e.g Part-time, Permanent, Contract)**   
**•	Company: Hiring Company**   
**•	Category: Job level Category (e.g IT-Jobs, Engineering)**   
**•	Salary_Range: salary range for the job, in thousands UK dollars.**  
**•	Salary: Salary paid, in thousands UK dollars, target variable.**    
**•Source_Name: Source of Job posting** 

## Data Preprocessing:

### Cleaning and Explanatory Data Analysis
![image](https://user-images.githubusercontent.com/77252878/133901449-c0e15da9-b498-4e4e-85b4-ced3ba1dd2e1.png)

### Checked for null values
![image](https://user-images.githubusercontent.com/77252878/133902382-880a7642-de6a-4019-b6a8-7793c3052252.png)
### Checked for duplicate values
![image](https://user-images.githubusercontent.com/77252878/133903045-4705b330-a40b-4fc1-8aa0-245cb6f2ab29.png)

Check for outliers Deleted the rows with salary < 0. Calculated the quantile value for 75% and 25%, the value above 75% - 210,000 tend to be outliers. Verified and validated the data as those rows are legitimate and those salary belongs to IT executive type jobs or from highly paid industry like oil and finance.

![image](https://user-images.githubusercontent.com/77252878/133904032-71eb83b3-3c06-40da-ac74-c4c0e496d139.png)

#### Fig X. Salary – target variable

In Fig X. we see, the target variable salary is somewhat right-skewed distribution, which is due to outliers and verified.
Performed explanatory data analysis to learn more about the relation between each feature and the target variable

### Salary versus Job Industry
![image](https://user-images.githubusercontent.com/77252878/133905204-bce43e3d-a9d2-44b8-932f-50bf5570a5dd.png)

#### Fig Y. Salary by Job Industry category
A clear difference is observed in the salary of different jobholders’ categories.  In Fig Y. we see, unsurprisingly,  a relatively strong relationship between the industry someone works in and the salary they make. Job Industry category and salary with the top 5 categories being Oil & Gas, IT jobs, Legal jobs, finance, and consulting jobs. Again unsurprisingly, those working part time made significantly less.

### Salary versus Contract Agreement
![image](https://user-images.githubusercontent.com/77252878/133905273-394a892e-0734-4004-82e2-5c7df3cdf377.png)
#### Fig Z. Salary by Job Contract
Permanent contract agreement seems to have higher salary

### Feature Engineering:

**Performed one-hot encoding for nominal categorical variable like category, contract-time and company.**

#### Checked for correlation:
![image](https://user-images.githubusercontent.com/77252878/133905406-1cea576d-19da-43f0-b29c-b8baed7ebab9.png)

Most of the features are positively correlated with the target variable salary and there is no evidence of multicollinearity of correlation > 0.6.

### Regression Models:

#### Used three models to train the model,
**•	Linear Regression**  
**•	Random Forest**     
**•	XGBoost**     

Trained the model with manual parameter and same model with k-fold(k=5) cross validation
![image](https://user-images.githubusercontent.com/77252878/133905506-44b867f5-c986-43ed-b392-5a14cbf5e32b.png)

From the above table, it shows XGBoost seems have lower root mean squared error without cross validation compared to the other two models(Linear regression and Random Forest), so performed hyperparameter tunning for XGBoost.
### Hyperparameter Tunning:
The mean squared error of hyperparameter tunned model is

![image](https://user-images.githubusercontent.com/77252878/133905541-86dfc753-a477-4f9a-90d7-f7e1b64fbc2b.png)
### Predicted Result:
The salary is predicted after learning the data from the trained dataset.

![image](https://user-images.githubusercontent.com/77252878/133905572-4137d715-b458-4399-9d82-5fd4a65741c6.png)
#### Feature importance:
Below is the feature importance for feature selection for further tunning the model.
![image](https://user-images.githubusercontent.com/77252878/133905642-cff56c14-ad36-4e0b-b4f0-e34b49e6f701.png)



























