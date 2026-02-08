# Skygeni_Anjana

# Sales Insight & Risk Alert System

## Overview
This project builds a lightweight Sales Insight and Alert System using historical CRM data.  
The goal is to help sales leaders understand *why* deals are being lost and proactively identify high-risk open deals before they fail.

The system focuses on explainable, business-friendly insights rather than complex models.

## Approach

1. **Exploratory Data Analysis (EDA)**  
   We analyzed historical deals to understand win and loss patterns across sales cycle length, deal stages, lead sources, regions, and sales reps.  
   A key finding was that deals with longer sales cycles are significantly more likely to be lost.

2. **Win Rate Driver Analysis**  
   Win rates were compared across different segments to identify low-performing regions, lead sources, and deal stages.  
   These comparisons helped uncover where deals typically break down.

3. **Rule-Based Risk Scoring Engine**  
   Using insights from historical data, a rule-based system was built to flag risky deals.  
   Each deal is scored based on:
   - Long sales cycle
   - Low-performing lead source
   - Low-performing region  

   These signals are combined into a simple risk score and mapped to:
   - Low Risk
   - Medium Risk
   - High Risk

4. **Insights, Alerts, and Automation**  
   The system generates:
   - Top high-risk open deals
   - Low-performing segments
   - Rep-level coaching signals  
   A weekly summary report and alerts can be generated automatically.

## How to Run the Project

1. requirements.txt - Install the libraries

2. Input Data

The system expects a CSV or DataFrame with the following columns:

deal_id,created_date,closed_date,sales_rep_id,industry,region,

product_type,lead_source,deal_stage,deal_amount,sales_cycle_days,outcome

3. Run the Pipeline (in Jupyter Notebook Part4_F6.ipynb)

result = weekly_sales_insight_job(df)

4. Scheduling (Optional)

For automation, the pipeline can be:
Run weekly using a Python scheduler (demo) - available in the same in Jupyter Notebook Part4_F6.ipynb

## Key Decisions

Rule-based system instead of ML:
Chosen for transparency, explainability, and ease of action. Sales leaders need to know why a deal is risky, not just a probability score.

Outcome used only for historical learning:
Deal outcomes are used only to learn patterns from past data.

Focus on business usefulness:
The system prioritizes actionable insights (alerts, risky deals, coaching signals) over predictive accuracy.

Designed for extensibility:
The rule-based engine can later be extended with ML models once more data and feedback are available.

