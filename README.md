# Power BI A/B Testing Analysis  
## Automated End-of-Contract Renewal Offers

## Project Overview

This project automated the renewal journey for customers approaching the end of their contract.

Eligible customers received a personalised email inviting them to renew their subscription for a further 18 months. The email included all contract information, a contract summary and a unique link to the company website, where the customer could accept the terms and conditions and submit the renewal without needing to call the contact centre.

The solution combined customer segmentation, A/B testing, automated communication and Power BI reporting to improve retention, increase recontract value and reduce manual work for the Loyalty team.

---

## Business Problem

The company was experiencing increased churn among customers **after the end of their contract**.

One of the main reasons was the price increase applied when the customer’s contractual discount ended. Renewals were also mainly handled by the Loyalty team through inbound and outbound calls, which created a high workload. This became increasingly difficult to manage as the company grew rapidly over the previous two years, tripling its customer base.

At the same time, the average revenue per user from recontracted customers was below forecast.

The company wanted to:

- Make the renewal process easier for customers
- Reduce churn after the end of contract
- Increase recontract ARPU
- Reduce inbound and outbound calls
- Improve long-term customer value
- Understand which offers worked best for different customer groups

---

## The Solution

I developed an automated process that identified customers close to the end of their contract and sent them a tailored renewal offer.

The offer was based on factors such as:

- Customer tenure
- Current package and speed
- Contract end date
- Competition available in the customer’s area
- Eligibility for a speed upgrade
- Discount level

Customers received either:

- An offer to renew on their current package and speed
- An offer to upgrade to the next available speed tier

---

## My Approach

### 1. Customer Selection

SQL was used to extract customer, service, pricing and contract information from the company database.

Customers were filtered based on their contract end date, service status and other eligibility rules.

Customers with an additional Wi-Fi device or a currently suspended service were excluded from all cohorts.

---
### 2. Cohort and Offer Logic
<table>
<tr>
<td width="35%" valign="top">
<p>Power BI combined data from different sources and applied the cohort rules.</p>
<p>Customers were grouped based on:</p>
<ul>
<li>Whether they were on their <strong>first or a subsequent contract</strong></li>
<li>Whether they lived in an <strong>overbuilt or non-overbuilt area</strong></li>
<li>Whether they were eligible for a <strong>speed upgrade</strong></li>
<li>The discount level included in the offer</li>
</ul>
<p>Customers were then split into a control group and different offer groups.</p>
<p>
<ul>
<li><strong>First-Contract Customers — Overbuilt Areas</strong> - Overall, 90% received an email.</li>
<li><strong>First-Contract Customers — Not-Overbuilt Areas</strong> - Overall, 90% received an email.</li>
<li><strong>Subsequent-Contract Customers</strong> - The same logic was used across overbuilt and non-overbuilt areas - Overall, 80% received an email.</li>
</ul>
</p><br>
<p>This structure allowed the business to compare the impact of discount level, speed upgrade and competition on renewal rate, churn and recontract ARPU.</p>
</td>
<td width="65%" valign="top">
<img src="images/Cohort%20Logic.png" alt="Customer cohort and offer logic" width="100%">
</td>
</tr>
</table>

---

### 3. Personalised Email Automation

Power Automate used the selected customer data to create and send personalised emails.

Each email included:

- Customer-specific information
- A tailored renewal offer
- Contractual renewal information
- A unique website link to accept the terms and conditions

---

### 4. Customer Acceptance

The customer has been provided with all the legal required information in the email to review the offer and complete the renewal without contacting the customer service team.

Once the customer accepted the offer, the automation updated Salesforce and created a record in the company database.

---

### 5. Tracking and Reporting

The records stored in Salesforce and the database were used to track performance and generate insights in Power BI.

The dashboards monitored:

- Emails sent
- Offers accepted
- Renewal rate
- Response rate
- Churn rate
- Recontract ARPU
- Performance by customer cohort
- Performance by offer
- Performance by competition level
- Performance by current-speed and upgrade offers

---

## Process Flow

![Project overview flow](images/Project%20Overview%20Flow.png)


---

## Tools Used

| Tool | Purpose |
|---|---|
| **SQL / PostgreSQL** | Extracted customer, service, pricing and contract data |
| **Power BI** | Combined data sources, created cohort logic and reported results |
| **Power Automate** | Created personalised emails and managed the automated workflow |
| **Salesforce** | Stored customer activity and renewal records |
| **Company Website** | Allowed customers to accept the offer |

---

## Results and Insights

<table>
<tr>
<td width="35%" valign="top">
<p>The project delivered clear commercial and operational improvements:</p>
<ul>
<li>The recontract rate for customers receiving the email was approximately <strong>double</strong> the rate of the control group</li>
<li>The one-click renewal email achieved a response rate of <strong>over 20%</strong></li>
<li>Customers offered an upgrade to the next speed tier achieved a response rate of <strong>over 30%</strong></li>
<li>Customers offered renewal on their current speed achieved a response rate of approximately <strong>20%</strong></li>
<li>Recontract ARPU became higher and more consistent</li>
<li>Churn reduced in areas with low competition but increased in areas with higher competion</li>
<li>The business gained a clearer view of how discount level and upgrade offers affected customer behaviour</li>
<li>Customers could renew without calling the contact centre</li>
<li>The Loyalty team stopped making renewal-related outbound calls, reducing their workload</li>
</ul>
<br>
<p>The strongest result came from the speed-upgrade offer. Customers were more likely to respond when the renewal included a clear improvement to their service, rather than only extending their existing package.</p>
</td>
<td width="65%" valign="top">
<img src="images/Analysis%20Overview.png" alt="Analysis Overview" width="100%">
</td>
</tr>
</table>

---

## Key Skills Demonstrated

- A/B testing and control-group analysis
- Customer segmentation
- Churn and retention analysis
- Commercial performance analysis
- Power BI data modelling and reporting
- SQL data extraction
- Workflow automation
- Salesforce integration
- Customer journey improvement
- Translating business requirements into a technical solution

---

## Suggested Screenshots

### Renewal Process

Add the process diagram showing how data moves between SQL, Power BI, Power Automate, Salesforce and the customer acceptance page.

### Cohort Logic

Add the cohort allocation visual showing the control group, Offer A, Offer B and upgraded-product groups.

### Renewal Performance Dashboard

Add the report showing:

- Monthly renewal volumes
- Recontract ARPU
- Performance by channel
- Performance by customer group

### Offer Acceptance Dashboard

Add the report showing:

- Emails sent
- Offers accepted
- Acceptance percentage
- Average accepted offer value
- Results by Offer A and Offer B

---

## Confidentiality Note

> The screenshots and information included in this portfolio have been anonymised. Customer data, company-sensitive information and confidential business rules have been removed or replaced.
