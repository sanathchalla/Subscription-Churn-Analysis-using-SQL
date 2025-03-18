# Codeflix Subscription Churn Analysis 🚀

## Project Overview
This project analyzes subscription churn rates for Codeflix, a streaming service, to help management understand user retention trends. Specifically, the marketing department is interested in comparing churn between two customer segments (Segment 87 and Segment 30).

Using SQL, this analysis determines the churn rate for both segments over the first three months of 2017 by tracking active and canceled subscriptions over time.

Column Name	Description
- id	Unique subscription ID
- subscription_start	Subscription start date
- subscription_end	Subscription end date (NULL if active)
- segment	User segment (87 or 30)
- Codeflix enforces a minimum subscription period of 31 days, ensuring that users cannot start and end their subscription in the same month.

## Objective:

Calculate the churn rate for each segment over January, February, and March 2017.
Compare churn rates between the two segments to determine which segment retains users better.

## Key Concepts Used
🔹 Aggregates – Used SUM() to count active and canceled subscriptions.

🔹 Unions – Combined data from different tables for analysis.

🔹 Temporary Tables – Created intermediate tables for better readability and organization.

🔹 Cross Joins – Combined all subscriptions with each month to track user activity.

🔹 CASE Statements – Categorized subscriptions as active or canceled based on conditions.

🔹 Aliasing – Used aliases to improve query readability.

🔹 Churn Rate Calculation – Defined as:

Churn Rate = Canceled Subscriptions/Active Subscriptions at Start of Month
 
## Key Steps in Analysis
✅ Data Exploration

Identified two customer segments: 87 and 30.
Determined the range of months available for churn calculation.
![Screenshot 2025-03-18 055931](https://github.com/user-attachments/assets/10be3765-b698-4ae0-aa34-7edfbdc7ddc3)
![Screenshot 2025-03-18 054318](https://github.com/user-attachments/assets/66efc0b4-1a04-4f32-b78b-bcd0291eddc0)

## ✅ Churn Calculation Process

## 1️⃣ Created a months table – Defined the first three months of 2017 as the analysis period.
![Screenshot 2025-03-18 061014](https://github.com/user-attachments/assets/a358696a-c616-4543-a934-b7f6c05e16ad)

## 2️⃣ Cross-joined months with subscriptions – Created a combined dataset to track user activity over time.
![Screenshot 2025-03-18 064846](https://github.com/user-attachments/assets/6d4d7355-037c-4249-be47-ca066d7e799e)

3️⃣ Labeled active subscriptions – Used CASE WHEN logic to track whether a user was active in a given month.
![Screenshot 2025-03-18 065942](https://github.com/user-attachments/assets/3a9f5046-07e1-41f0-96db-917031521e92)

4️⃣ Identified churned users – Marked users as canceled if their subscription ended within the given month.
5️⃣ Aggregated subscription data – Summed active and canceled subscriptions per segment for each month.
![Screenshot 2025-03-18 071116](https://github.com/user-attachments/assets/b9ac981b-6b28-483b-8ee8-9e6a58d4bd6d)


6️⃣ Calculated churn rate – Used the formula above to measure retention.
![Screenshot 2025-03-18 071902](https://github.com/user-attachments/assets/244901dd-3476-492a-9ac0-eb56915c0cd8)

## ✅ Insights & Findings

Segment X had a lower churn rate than Segment Y (replace with actual segment numbers after analysis).
Marketing teams can use these insights to optimize retention strategies.

## SQL Queries Used:
This project was implemented using SQL to manipulate and analyze subscription data. Key techniques include:

JOINs & CROSS JOINs
CASE WHEN statements
Aggregations (SUM, COUNT)
Temporary Tables & Aliasing

## Technologies Used:
🗄️ SQL – Data retrieval, transformation, and analysis
📊 Data Visualization – (Optional, if you created visual reports)
