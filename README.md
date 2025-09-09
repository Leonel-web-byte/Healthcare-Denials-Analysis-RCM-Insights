# 🏥 Context

We are into the denial management step of **Revenue Cycle Management (RCM)** right after the payment was posted by the Payer. We want to have an overview of denial claims before resubmitting them. For this, we are analyzing three denial rates: **Claim Denial rate (CDR)**, **Revenue Denial Rate (RDR)** and **Recoverable Revenue Denial Rate (RecRDR)** over Payer and Department. By doing this, we will be able to show which Payer or Department is making us lose the most money, where we can get Return of Investment fast, and where our coding team and billing are making a lot of mistakes.

👩‍💻 **Developer:** Leonel Djouokep  
📌 **Subtitle:** SQL + Excel Portfolio Project 

📌 **Interactive Dashboard file** <a href= "https://github.com/Leonel-web-byte/Healthcare-Denials-Analysis-RCM-Insights/blob/main/PowerPivot.xlsx"> Click here</a>


## 📊  Data Cleaning
-	I removed 22 duplicate claims from the dirty dataset
-	Standardized dataset format and formatting currency to 2 decimal places.
-	Standardized date format to MM/DD/YYYY
-	Applied business logic checks (e.g., Paid ≤ Allowed ≤ Claim Amount)
-	Capped claims Amount and Allowed Amount at minimum values where the business logic was not respected.
-	Created a new column called “capping”, which is filled with three categories: “Normal claim” for claim with not discrepancies, “Capped at Billed” while Allowed > Claim Amount and “Capped at Allowed” while Paid>Allowed.
  
**Cleaned dataset**: <a href= "https://github.com/Leonel-web-byte/Healthcare-Denials-Analysis-RCM-Insights/blob/main/Cleaned%20Dataset_Power.xlsx"> View Dataset</a>


## 🎯 Project Goals

- Build dashboards to monitor denial rates, trends, payer and department patterns.
- Analyze top denial reasons and financial impact.
- Provide denial management with easy-to-read KPIs.
- Highlight recoverable money and preventable denials.

## 🧠 KPIs

- **Claim denial rate** (CDR)
- **Revenue denial rate** (RDR)
- **Recoverable denial rate** (RecDR)
- **Money at risk**
- **Preventable denial claims rate**

  ## 🧱 Database Schema
  I  worked with 5 main tables:  
 
## 🧩 SQL/Ad-Hoc Analysis

 I wrote modular `.sql` scripts for different parts of the analysis:
 
 - 01_data.sql → row counts, distinct statuses
   
 This helped me answer questions like:
 - **Summary metrics** (**Total claims**, **RDR**, **RecDR**, **CDR**, **Money at risk**, **Preventable Denial claims**)
- **Where are we losing money and why?** 
- **Where are we making mistakes and why?** 
- **Where should we spend recovery resources for best ROI?** 
-	**Which denial reasons are most frequent and financial impact of them?**

## 📊 Excel Dashboard Design
The dashboard brings the SQL findings to life with visuals:  

<img width="549" height="279" alt="Claims_P" src="https://github.com/Leonel-web-byte/Healthcare-Denials-Analysis-RCM-Insights/blob/main/Dashboard.png" />

 ## 📌Key Insigths
 👉 **37.81%** of all denied claims comes from the **Pediatrics** department and **36.46%** comes from the **Orthopetics** department.
 
 👉 **34.30%** of all denied claims comes from **Blue cross** and **33.85%** comes from **UnitedHealthcare**.

 👉 The hospital faces a potential loss of **$149,999.99**, with only **$8,097.87** recoverable.

 👉 The claim denial rate is **32.50%**, of which **23%** was preventable.

 👉 In the **Pediatrics** department, **duplicate claims** are the main root cause of claim denials, resulting in a loss of  **$4949.81**, followed by **coding errors**, which result in a loss of **$4667.53.**

👉 **Timely Filing** is the main root cause of claim denials in the **Orthopetics** department, resulting in a loss of **$7540.18**.

## 📌 Actionable Insights
Because the recoverable Revenue Denial Rate is low accross all departments and payers, the first action to take in order to reduce the **denial rate** and recover some return on investment **(ROI)** is:

✅ Systematically Train Billing and Coding Team on how to avoid duplicate claims, perform accurate coding and submit claims on time.

✅ Review payer policies, as many denied claims are not recoverable.

✅ Deploy our Appeals team equitably across all departments, as the Recoverable Revenue Denial Rate **(RecRDR)** is nearly the same throughout all departments.

  ## 🛠️ Tools Used
- **SQL**: PostgreSQL 
- **Visualization**: Power Pivot Excel 
- **Slicers for quick filtering by Month, Payer, and Department**: Slicers 

  ## 📬 Contact
**Leonel Djouokep**  
📌 Open to data analytics roles | Excel • SQL • Tableau • Data Visualization

📌 **Email**: gautier.l.djouokep@gmail.com
