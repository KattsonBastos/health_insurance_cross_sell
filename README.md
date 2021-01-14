# Health Insurance Cross Sell: making the company to sell more with Machine Learning

<p align='center'>
<img src="/imgs/banner.jpg" alt="drawing" width="90%"/>
</p>
<p align='center'>
<a href="http://www.freepik.com">Designed by rawpixel.com / Freepik</a>
</p>
                                                
_until the project get finished, this README will contain the problem and the steps to be done._

## A Brief on the Business Demand
:warning: Fictional Context :warning:
Insurance All is a company that provides health insurance to its customers. They're analyzing the possibility of offering policyholders a **new product**: **vehicle insurance**.
In the actual company's agreement policy, the pays anually for the insurance. Thus, the company whants to replicate this policy to the vehicle insurance.

- **How will they offer the product to customers**: phone calls (capacity for 20,000 phone calls during the campaign);
- **how they got the customer's interest on joining a new product**: a survey of about 380,000 customers;
- **How many new customers will participate in the offering campaign**: 127,000.

Our Data Science team was hired to build a model that predicts **whether or not the customer would be interested in auto insurance**, so the Sales Team hopes to be able to **prioritize** the people with the greatest interest in the new product and thus **optimize the campaign** by making only contacts with customers most likely to make the purchase.

**Questions we have to answer:**<br>
- Main insights on the most relevant attributes of customers interested in purchasing auto insurance.
- What percentage of customers interested in purchasing vehicle insurance will the sales team be able to reach by making 20,000 calls?
- And if the sales team's capacity increases to 40,000 calls, what percentage of customers interested in purchasing vehicle insurance will the sales team be able to contact?
- How many calls does the sales team need to make to contact 80% of customers interested in purchasing vehicle insurance?

**Understanding the demand**<br>
- **The root cause of the demand:** to offer the vehicle insurance so that the sales team makes more calls to customers who are interested in purchase hte product.
- **Stakeholders:** the company's Sales team
- **Product Delivering Method:** 
    - **Granularity:** unique customers data
    - **Business Model:** Cross Sell - classification prolem
    - **Main Methods:** Classification Machine Learning Models
    - **Solution presentation:** Dashboard with the classifications and insights; and provide the model so the Sales team could make requisitions and get the classification of new clients.
    
---
## Project Steps
* [x] **Sprint 01** (05/01)
    - [x] Business Demand Understanding
    - [x] Initial Hypothesis Creation
    - [x] Solution Planning
    - [x] Data Collection
* [ ] **Sprint 02** (12/01)
    - [x] Descriptive Analysis
    - [x] Business Research
    - [ ] Hypothesis Creation and Feature Engineering
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
## A Brief on the Company's Business Model
The insurance sector is all about taking and managing risks. Thus, offering a new product (vehicle insurance) means taking more risk.
_offer a new product (vehicle insurance) means taking more risk)_

### What is an Insurance and How It Works
Insurance is a contract, represented by a policy, in which an individual or entity receives financial protection or reimbursement against losses from an insurance company [reference](https://www.investopedia.com/terms/i/insurance.asp).
The basic concept of insurance is that one party, _the insurer_, will guarantee payment for an uncertain future event, and the insured or the policyholder, pays a _premium_ to the insurer in exchange for that protection on that uncertain future occurrence.

The _premium_ is basically the price of the insurance, tipically expressed as a monthly or annually cost. It is based on the customer's risk profile.

According to [this article](https://en.wikipedia.org/wiki/Vehicle_insurance#Coverage_levels), the premium can vary depending on many factors that are believed to affect the expected cost of future claims. Some of those factors are: _gender, age, driving history, marital status, profession, vehicle classification, neighbourhood, behavior-base and even the credit rating_.

### The Insurance Sector
Insurance companies base their business models around **assuming** and **diversifying risk.**
They generate revenue in two ways: **Charging premiums** in exchange for insurance coverage, then **reinvesting** those premiums into other _interest-generating_ assets.
The **insurer's real product** is the customer claims. Thus, the company must process when the customers files them and then check their accuracy and submit the payments.

The main reason why insurance works is because the likelihood of something unfortunate happen to the insured is low ([reference](https://www.hioscar.com/blog/how-health-insurance-works-risk-sharing)). However, it's not the same between all insurance types. 

**health insurance**<br>
It is an insurance that covers the whole or a part of the risk of a person incurring _medical expenses_, spreading the risk over numerous persons.
Differently than others, health insurance is used more often.

**vehicle insurance**<br>
It provides financial protection against _physical damage_ or _bodily injury_ resulting from traffic collisions and against liability that could also arise from incidents in a vehicle. It covers many types of vehicles, like _cars_, _trucks_, and _motorcycles_. It can also cover against non-traffic events, like _theft_, _natural disasters_, and _weather_.

---
## Initial Hypothesis
🔸_Creation in progress_🔸

| **Hypothesis** | **Description** |
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
