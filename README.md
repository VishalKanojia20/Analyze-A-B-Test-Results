# Analyze-A-B-Test-Results
A/B tests are commonly performed by data analysts and data scientists.
For this project, I will be working to understand the results of an A/B test run by an e-commerce website.The company has developed a new web page in order to try and increase the number of users who "convert," meaning the number of users who decide to pay for the company's product. My goal is to work through this notebook to help the company understand if they should implement the new page, keep the old page, or perhaps run the experiment longer to make their decision.

**This project is divided into 3 parts:**
>01. Probability.
>02. AB Testing.
>03. Regression. 

**Requirements for this project:**
01. A csv file for the stored data. 
02. Python libraries like Numpy, Pandas, Matplotlib and Random. 
The csv file I used for this project is **ab_data.csv** which was provided to me by Udacity. 
There are 294487 enteries in the dataset out of which 290584 are unique. There are 4 columns - user_id, timestamp, group, landing_page, converted. 

### 1. Probability:
In this part, I computed the probability for the users in the control group getting converted and the users in the treatment group getting converted. I used .query(), .mean() and .drop() functions to calculate the probabilities. 
### 2. AB Testing:
For this part, I assumed two hypothesis
> ***Ho : Pold >= Pnew*** 
> ***H1 : Pold < Pnew***
Then performed the sampling distribution for the difference in **converted** between the two pages over 10,000 iterations of calculating an estimate from the null. I used the concept of **p-value** to get to the conclusion based on the hypothesis. 
### 3. Regression:
For this part, I used **statsmodel** library of Python and performed regression modelling (majorly Logistic Regression)for the users from different countries to decide that whether the company should launch the new web page or not or should run the experiment for a little longer duration. 
