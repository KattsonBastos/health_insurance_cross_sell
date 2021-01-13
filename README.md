# Health Insurance Cross Sell: making the company to sell more with Machine Learning

<p align='center'>
<img src="/imgs/banner.jpg" alt="drawing" width="90%"/>
</p>
<p align='center'>
<a href="http://www.freepik.com">Designed by rawpixel.com / Freepik</a>
</p>
                                                
_until the project get finished, this README will contain the problem and the steps to be done._

## A brief on the business demand
:warning: Fictional Context :warning:
Insurance All is a company that provides health insurance to its customers. They're analyzing the possibility of offering policyholders a **new product**: **vehicle insurance**.
In the actual company's agreement policy, the pays anually for the insurance. Thus, the company whants to replicate this policy to the vehicle insurance.

- **How will they offer the product to customers**: phone calls (capacity for 20,000 phone calls during the campaign);
- **how they got the customer's interest on joining a new product**: a survey of about 380,000 customers;
- **How many new customers will participate in the offering campaign**: 127,000.

Our Data Science team was hired to build a model that predicts **whether or not the customer would be interested in auto insurance**, so the Sales Team hopes to be able to **prioritize** the people with the greatest interest in the new product and thus **optimize the campaign** by making only contacts with customers most likely to make the purchase.

**Questions we have to answer:**
- Main insights on the most relevant attributes of customers interested in purchasing auto insurance.
- What percentage of customers interested in purchasing vehicle insurance will the sales team be able to reach by making 20,000 calls?
- And if the sales team's capacity increases to 40,000 calls, what percentage of customers interested in purchasing vehicle insurance will the sales team be able to contact?
- How many calls does the sales team need to make to contact 80% of customers interested in purchasing vehicle insurance?

**Understanding the demand**
- **The root cause of the demand:** offer a new product to customers
- **Stakeholders:** the company's Sales team
- **Product Delivering Method:** 
    - **Granularity:** unique customers data
    - **Business Model:** Cross Sell - classification prolem
    - **Main Methods:** Classification Machine Learning Models
    - **Solution presentation:** Dashboard with the classifications and insoghts; and the model so new classifications could be mande.
    
---
## Project Steps
* [ ] **Sprint 01** (05/01)
    - [x] Business Demand Understanding
    - [x] Initial Hypothesis Creation
    - [x] Solution Planning
    - [x] Data Collection
* [ ] **Sprint 02** (12/01)
    - [ ] Descriptive Analysis
    - [ ] Business Research
* [ ] **Sprint 03** (19/01)
    - [ ] Exploratory Data Analysis
    - [ ] Insights Report
* [ ] **Sprint 04** (26/01)
    - [ ] Data Preparation
    - [ ] Feature Selection
* [ ] **Sprint 05** (02/02)
    - [ ] Machine Learning Model
* [ ] **Sprint 06** ( 09/02)
    - [ ] Business Metrics Creation
    - [ ] Translating and Interpreting the Metrics
* [ ] **Sprint 07** (16/02)
    - [ ] Model Deployment
* [ ] **Sprint 08** (23/02)
    - [ ] Accessing Data in Production
* [ ] **Sprint 09** (02/03)
    - [ ] Presentation to the Business Team
* [ ] **Sprint 10** (09/03)
    - [ ] article creation
    - [ ] What we learn

---
## Initial Hypothesis

_The following hypothesis list will be updated in the second sprint of this project, when the company's business model will be properly understood._

| Hypothesis | Description |
| --- | --- |
| H1 | Customers who have had purchased an insurance (like life insurance) are more likely to purchase the vehicle's one |
| H2 | The longer the customer has had an insurance, the more likely he/she is to purchase the insurance |
| H3 | Older customers are more likely to purchase the vehicle insurance | 
| H4 | The younger the customer's vehicle, the more likely he/she is to purchase the insurance | 
| H5 | Customers with a bad vehicle accident history are more likely to purchase the insurance | 
| H6 | The higher the client's income, the more likely he/she is to purchase the insurance | 
| H7 | Customers from urban areas are more likely to purchase the insurance  | 

---
## The Dataset
_this is from Kaggle problem description, but it'll be changed after the data collection_

### Data information:

**User Level Data**

| Variable | Type | Description |
| --- | --- | --- |
| **Id:** | Discrete | customer's unique ID. |
| **Gender:** | Discrete | customer's gender. |
| **Age:** | Discrete | customer's age. |
| **Policy sales channel:** | Discrete | anonymous code for the customer contact channel. |
| **Region Code:** | Discrete | customer's region code. |

 **Vehicle Level Data**
 
| Variable | Type | Description |
| --- | --- | --- |
| **Id:** | Discrete | customer's unique ID. |
| **Driving License:** | Binary | 0, the customer is not allowed to drive; and 1, the customer is allowed to drive. |
| **Vehicle Age:** | Discrete | vehicle age |
| **Vehicle Damage:** | Binary | 0, the customer has never had his vehicle damaged in the past; and 1, the customer has had their vehicle damaged in the past. |

**Insurance Level Data**

| Variable | Type | Description |
| --- | --- | --- |
| **Id:** | Discrete | customer's unique ID. |
| **Anual Premium:** | Continuous | amount the customer paid the company for annual health insurance. |
| **Vintage:** | Discrete | number of days the customer joined the company through the purchase of health insurance. |
| **Previously Insured:** | Binary | 0, the customer does not have auto insurance; and 1, the customer has had auto insurance. |
| **Response:** | Binary | 0, the customer is not intereste; and 1, the customer is interested. |

<p align='center'>
<img src="/imgs/schema_diagram.png" alt="drawing" width="90%"/>
</p>
