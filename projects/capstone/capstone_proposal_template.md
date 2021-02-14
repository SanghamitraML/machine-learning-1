# Machine Learning Engineer Nanodegree
## Predict Home Credit's Default Rate

Sanghamitra Bhattacharjee
February 14th, 2021

### Proposal

### Domain Background

In this section, provide brief details on the background information of the domain from which the project is proposed. Historical information relevant to the project should be included. It should be clear how or why a problem in the domain can or should be solved. Related academic research should be appropriately cited in this section, including why that research is relevant. Additionally, a discussion of your personal motivation for investigating a particular problem in the domain is encouraged but not required.

Credit risk is the possibility of a loss resulting from a borrower's failure to repay a loan or meet contractual obligations. Traditionally, it refers to the risk that a lender may not receive the owed principal and interest. Although it's impossible to know exactly who will default on obligations, properly assessing and managing credit risk can lessen the severity of a loss. Interest payments from the borrower or issuer of a debt obligation are a lender's or investor's reward for assuming credit risk. In recent times, the US subprime crisis is an example of huge financial crisis. In essence the core reson for the financial crisis was a broader trend of lowered lending standards and higher-risk mortgage products. Insufficient understand of credit risk can become a problem of huge proportions. Ont he other hand too much tightening of lending will exclude people from lower income groups from organized banking. The solution is to find a balanced solution which will enable more and more people to access credit while providing a complete understanding of the risk involved.

Home credit focusses on providing small loans to people with little or no credit history.

Research Papers https://www.centerforfinancialinclusion.org/new-credit-risk-models-for-the-unbanked

https://development.asia/explainer/heres-how-alternative-credit-scoring-can-improve-poors-access-loans

https://www.mckinsey.com/business-functions/risk/our-insights/new-credit-risk-models-for-the-unbanked#

https://www.imf.org/en/Publications/WP/Issues/2020/09/25/Fintech-Credit-Risk-Assessment-for-SMEs-Evidence-from-China-49742

Data Source

This is a featured competition is Kaggle and I will be using the data set from Kaggle. https://www.kaggle.com/c/home-credit-default-risk/overview

### Problem Statement

In this capstone project, I will build a model that will predict the probability of an applicant to repay their loan. 
The applicant population being considered for this project are people with little or no credit history. Due to this the risk of lending to this segment is traditionally considered very high. They often get exclused from formal banking. However with the advances in Data analysis and machine learning, we have the opportunity to go beyond traditional risk analysis and use data other than credit history to understand better the ability of an applicant to repay the loan.
A good ML model with help provide credit to this underserved segment as well as lower the crdit risk for the lending organization in this case Home Credit.
Considering the consequences of nonrepayment of loans, it is important for the model to minimize false positives.


### Datasets and Inputs
This dataset has been provided by Home Credit for Kaggle.

There are 7 different sources of data:

1. application_train/application_test: The main training data with information about each loan application at Home Credit. Every loan has its own row and is identified by the feature SK_ID_CURR. The training application data comes with the TARGET indicating 0: the loan was repaid or 1: the loan was not repaid. Here we will use only the Training data.
2. bureau: In this dataset it consists of data concerning client’s previous credits from other financial institutions. Each previous credit has its own row in bureau, but one loan in the application data can have multiple previous credits.
3. bureau_balance: It consists of monthly data about the previous credits in bureau. Each row is one month of a previous credit, and a single previous credit can have multiple rows, one for each month of the credit length.
4. previous_application:The data of previous applications for loans at Home Credit of clients who have loans in the application data. Each current loan in the application data can have multiple previous loans. Each previous application has one row and is identified by the feature SK_ID_PREV.
5. POS_CASH_BALANCE: It consists of monthly data about previous point of sale or cash loans clients have had with Home Credit. Each row is one month of a previous point of sale or cash loan, and a single previous loan can have many rows.
6. credit_card_balance:The monthly data about previous credit cards clients have had with Home Credit. Each row is one month of a credit card balance, and a single credit card can have many rows.
7. installments_payment:The data of payment history for previous loans at Home Credit. There is one row for every made payment and one row for every missed payment.

### Solution Statement
_(approx. 1 paragraph)_

In this section, clearly describe a solution to the problem. The solution should be applicable to the project domain and appropriate for the dataset(s) or input(s) given. Additionally, describe the solution thoroughly such that it is clear that the solution is quantifiable (the solution can be expressed in mathematical or logical terms) , measurable (the solution can be measured by some metric and clearly observed), and replicable (the solution can be reproduced and occurs more than once).

### Benchmark Model
I am proposing to use the scores of the contestants of the Kaggle competition as the benchmark result. There is no openly available benchmark model to compare against.

### Evaluation Metrics
Since the data available to us is an Imbalanced Dataset, we cannot simply use Accuracy as a metric for evaluating the performance of the model. There are some metrics that work well with imbalanced datasets, of which we will use the below-mentioned metrics.
ROC-AUC Score: This metric is insensitive to class imbalance. It works by ranking the probabilities of prediction of the positive class label and calculating the Area under the ROC Curve which is plotted between True Positive Rates and False Positive Rates for each threshold value.
Recall Score: It is the ratio of the True Positives predicted by the model and the total number of Actual Positives. It is also known as True Positive Rate.
Precision Score: It is the ratio of True Positives and the Total Positives predicted by the model.
Image for post
Recall and Precision Score Formulae
Confusion Matrix: The confusion matrix helps us to visualize the mistakes made by the model on each of the classes, be it positive or negative. Hence, it tells us about misclassifications for both classes.

### Project Design
_(approx. 1 page)_

In this final section, summarize a theoretical workflow for approaching a solution given the problem. Provide thorough discussion for what strategies you may consider employing, what analysis of the data might be required before being used, or which algorithms will be considered for your implementation. The workflow and discussion that you provide should align with the qualities of the previous sections. Additionally, you are encouraged to include small visualizations, pseudocode, or diagrams to aid in describing the project design, but it is not required. The discussion should clearly outline your intended workflow of the capstone project.

-----------

**Before submitting your proposal, ask yourself. . .**

- Does the proposal you have written follow a well-organized structure similar to that of the project template?
- Is each section (particularly **Solution Statement** and **Project Design**) written in a clear, concise and specific fashion? Are there any ambiguous terms or phrases that need clarification?
- Would the intended audience of your project be able to understand your proposal?
- Have you properly proofread your proposal to assure there are minimal grammatical and spelling mistakes?
- Are all the resources used for this project correctly cited and referenced?
