# Lending Club

EDA to understand how consumer attributes and loan attributes influence the tendency to default

## Table of Contents

- [General Info](#general-information)
- [Technologies Used](#technologies-used)
- [Conclusions](#conclusions)
- [Acknowledgements](#acknowledgements)

---

## General Information

When a loan application is received, the company must make a loan approval decision based on the applicant's profile. The bank's decision is associated with two types of risks:

- If the applicant is likely to repay the loan, then the company loses business by not approving the loan.
- If the applicant is unlikely to repay the loan, i.e. if he or she will default, approving the loan may result in a financial loss for the company.

The loan dataset contains information about previous loan applicants and whether they 'defaulted' or not. The goal is to identify patterns that indicate whether a person is likely to default, which can then be used to take actions such as denying the loan, reducing the loan amount, lending (to risky applicants) at a higher interest rate, and so on.

<img src="images/loan_dataset.png" alt="Loan Dataset Image" width="50%">

When a person applies for a loan, the company may make one of two decisions:

1. Loan accepted: If the loan is approved by the company, there are three possible outcomes as described below:
   - Fully paid: The applicant has paid off the loan in full (the principal and the interest rate)
   - Current: The applicant is in the process of paying the installments, so the loan's tenure has not yet been completed. These candidates are not marked as 'defaulted'.
   - Charged-off: The applicant has not paid the installments on time for an extended period of time, indicating that he or she has defaulted on the loan.
2. Loan rejected: The loan had been rejected by the company (because the candidate does not meet their requirements etc.). Because the loan was rejected, the applicants have no transactional history with the company, and thus this data is not available to the company (and thus in this dataset)

### Dataset

- [Loan Data Set](https://cdn.upgrad.com/UpGrad/temp/3ba74fb7-bd88-4854-8597-1c225a5aed99/loan.zip): This contains the complete loan data for all loans issued through the time period 2007-2011.
- [Data Dictionary](https://cdn.upgrad.com/UpGrad/temp/af860da6-f838-47d6-ad97-551022550ee4/Data_Dictionary.xlsx): This dataset describes the meaning of the variables mentioned in the Loan Data Set.

---

## Technologies Used

Python 3.8.10
| Library | Version |
| ---------- | ------- |
| matplotlib | 3.5.3 |
| numpy | 1.22.4 |
| pandas | 1.3.5 |
| seaborn | 0.11.2 |

---

## Conclusions

- Term has the most impact on default rate, loan term being 60 months are 2.5x more likely to default than 36 months. 
- Loan Grades A through G shows a pattern of increased risk. 
- Employment Length does not show much impact on default rates. 
- Verification Status being source verified and verified slightly increases the default rate.
- Home ownerships being stated mortgaged, owned or rented, very slightly increases the default risk in the order. Mortgaged being the least. 
- Higher the interest rate, higher is the risk of default.
- Higher annual income may very slightly reduce the risk of defaulting the loan.
- As DTI(Debt-To-Income) ratio increases, the risk of default increases as well.

---

## Acknowledgements

- This case study was done as a part of EPGP ML & AI, IIIT-B.
- [Loan Data Set](https://cdn.upgrad.com/UpGrad/temp/3ba74fb7-bd88-4854-8597-1c225a5aed99/loan.zip) and [Data Dictionary](https://cdn.upgrad.com/UpGrad/temp/af860da6-f838-47d6-ad97-551022550ee4/Data_Dictionary.xlsx) was provided by upGrad and IIIT-B.

---

Case Study done by: 
- [Rahul Nanwani](https://github.com/rahul-nanwani)
- [Nitin Katiyar](https://github.com/nitink08)
