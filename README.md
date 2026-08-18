# African Gig Economy & Digital Wallet Report

**Analysis Period: 2023–2024**

---

## Executive Summary

Africa loses an estimated **$4 billion annually to scams and cyber fraud**. Within the four markets covered in this dataset, Kenya has also experienced significant digital-fraud exposure. According to *Eastleigh Voice*, **2.3% of transaction attempts involving Kenyan consumers in 2025 were suspected of digital fraud**, below the global average of 3.8% but the second-highest rate among the African countries analyzed, behind South Africa.

For the period **2023–2024**, this analysis examines transactions conducted through different channels and the workers operating across four African markets. The analysis focuses on:

- Transaction performance
- Fraud exposure
- Market performance
- Channel performance
- Worker risk

---

## Dataset Structure
To download the dataset as well as the project guiding details [Click here](https://datadna.onyxdata.co.uk/challenges/august-2026-datadna-african-gig-economy-and-digital-wallet-analytics-challenge/)
 
The dataset contains:

- **4 Dimension Tables**
  - Channel
  - Market
  - Dates
  - Workers
- **1 Fact Table**
  - Transaction History

### Tables

| Table | Description |
|---|---|
| **Channel** | Contains the different channels and sub-channels through which transactions were made |
| **Market** | Contains the four markets covered in the dataset |
| **Dates** | Contains the dates and periods covered by the transaction data |
| **Workers** | Contains worker information including gig segment, risk score, demographics, and activity status |
| **Transaction History** | Contains all transactions recorded during the analysis period |

---

# Project Objectives

## Transactions

1. Determine:
   - Total amount transacted
   - Fraudulent transactions
   - Total transactions
   - Fraud loss
   - YoY change
2. Identify which markets recorded the highest transaction activity.
3. Identify which channels recorded the highest transaction activity.
4. Analyze the monthly transaction trend.

## Risks

1. Determine the average worker risk score.
2. Analyze risk scores by market.
3. Analyze risk scores by gender.
4. Identify the age band with the highest risk score.
5. Analyze the monthly trend in risk scores.

## Workers

1. Determine the total number of workers and active workers.
2. Calculate average account tenure.
3. Categorize workers into risk levels.

---

# Dashboard Preview

### Relationships
<img width="860" height="440" alt="Relationships" src="https://github.com/user-attachments/assets/76d61e2b-659a-4983-8f13-63101b66e848" />

### Transactions

<img width="737" height="411" alt="Transactions" src="https://github.com/user-attachments/assets/6ea954c8-362e-422e-bdc8-d17967faefa9" />

### Risks

<img width="676" height="377" alt="Risks" src="https://github.com/user-attachments/assets/bb4acbfc-9409-4ece-8ae1-36e66c009a22" />


### Workers

<img width="727" height="407" alt="Workers" src="https://github.com/user-attachments/assets/06e8d536-8e88-4f43-8107-e794a667598b" />





---

# Analysis Findings

## Transactions

- There were **50,000 transactions**, representing a **1.4% increase** from the previous year.
- **25,145 transactions (50.3%) were flagged as fraudulent**.
- Fraudulent transaction counts increased by approximately **2.0% YoY**.
- The total amount transacted was **$24.98 million**, representing a **0.7% increase** from the previous year.
- **$12.56 million** was associated with fraudulent transactions, representing a **1.5% increase** from the previous year.
- **Ghana** recorded the highest share of transaction activity at **25.3%**, followed by:
  - South Africa: **25.0%**
  - Kenya: **25.0%**
  - Nigeria: **24.8%**
- Ghana also recorded the highest share of flagged fraudulent transactions at **25.5%**, followed by:
  - Kenya: **25.0%**
  - Nigeria: **24.8%**
  - South Africa: **24.7%**

### Transaction Channels

| Channel | Share of Transactions |
|---|---:|
| Agent | **25.0%** |
| POS | **25.0%** |
| API / Third-Party | **24.7%** |
| Mobile App | **17.0%** |
| USSD | **8.5%** |

---

# Risk Analysis

- The average worker risk score was approximately **50.4**.
- Risk scores were segmented into four categories:
  - **Low:** 0–25
  - **Moderate:** >25–50
  - **High:** >50–75
  - **Critical:** >75–100
- Approximately:
  - **25.0%** of workers were classified as Low Risk
  - **23.9%** as Moderate Risk
  - **25.4%** as High Risk
  - **25.7%** as Critical Risk
- Average worker risk scores were relatively similar across gender groups, ranging from approximately **49.9 to 51.0**.
- **USSD recorded the highest fraud rate at approximately 51.2%**.
- **POS recorded the highest fraud volume rate at approximately 51.4%**.

---

# Worker Analysis

- The dataset contains **5,000 workers**.
- **2,441 workers are active**, representing approximately **48.8%** of the worker population.
- Active workers averaged approximately **20.5 transactions per worker**.

### Worker Metrics

| Metric | Value |
|---|---:|
| Total Workers | **5,000** |
| Active Workers | **2,441** |
| Active Worker Rate | **48.8%** |
| Average Transactions per Active Worker | **20.5** |

---

# Recommendations

### 1. Strengthen Fraud Detection and Prevention

The high level of fraud flags and fraud-related transaction value indicates a need for stronger transaction monitoring and fraud prevention mechanisms.

Recommended actions include:

- Real-time fraud monitoring
- Automated transaction alerts
- Transaction velocity monitoring
- High-value transaction verification
- Enhanced identity and account verification

### 2. Prioritize High-Risk Channels

POS, Agent, and API/Third-Party channels account for a significant proportion of transaction activity.

Particular attention should be given to **POS and USSD**, which recorded elevated fraud exposure.

### 3. Investigate Increasing Fraud Value

Fraudulent transaction value increased even as transaction growth remained relatively modest.

Management should investigate:

- Average fraudulent transaction value
- High-value fraudulent transactions
- Fraud concentration by worker
- Fraud concentration by channel
- Fraud trends over time

### 4. Implement Worker-Level Risk Segmentation

Workers should be segmented into **Low, Moderate, High, and Critical** risk categories.

The business can then investigate whether high-risk workers are associated with:

- Higher fraud rates
- Higher fraud losses
- Higher transaction activity
- Specific transaction channels

### 5. Evaluate Digital Channel Adoption

Mobile App and USSD represent smaller shares of overall transaction activity.

Their performance should be compared against traditional channels using:

- Transaction volume
- Fraud rate
- Fraud volume rate
- Processing time
- Average transaction value

Where digital channels demonstrate lower risk and acceptable performance, businesses can encourage greater adoption.

---

# Power BI Analysis

## Key KPIs

The dashboard focuses on the following KPIs:

- Total Transaction Volume
- Total Transactions
- Active Workers
- Average Transaction Value
- Fraudulent Transactions
- Fraud Rate
- Fraud Loss
- Fraud Volume Rate
- YoY Transaction Growth
- Average Transactions per Active Worker

---

# DAX Measures Reference

**YOY change measures**: shows the percentage increase or decrease from the previous year(2023) <br>
1.	Amount lost
2.	Transactions, total amount, fraudulent transactions
3.	Fraud rate
4.	Reversed transactions

\
**Workers' Measures:**
1.	Active Worker
2.	Average Transactions per active worker

\
**Added Column**
1.	Risk Categories: categories the risk scores into 4.
-	Critical
-	High
-	Moderate
-	Low 
