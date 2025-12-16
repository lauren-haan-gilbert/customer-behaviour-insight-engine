# Customer Behaviour Insight Engine

A data analytics project that explores customer behaviour, session journeys, and conversion funnels using clickstream-style data.  
Built with **Python** and **SQL** to demonstrate how raw event data can be transformed into actionable insights about user journeys and drop-off points.

---

## Project Overview

This project simulates how a digital organisation (e.g. e-commerce or content platforms) can analyse user behaviour across sessions to understand:

- How users move through a site  
- Where they drop off in the funnel  
- How behaviour differs by device, country, or session characteristics  
- Why simple *one-session* analyses are often insufficient  

The focus is not just on metrics, but on **behavioural patterns and journeys**.

---

## Key Questions Explored

- What are the most common session paths through the site?
- Where do users drop off between key steps  
  *(view → cart → checkout → purchase)*?
- How do conversion rates differ by device or country?
- When is session-level analysis sufficient — and when does customer-level analysis become necessary?
- What are the limits of association rule mining (Apriori) when most sessions contain only a single checkout or purchase?

---

## Data

The project uses structured CSV data representing a simplified clickstream model:

- **events** – raw user events (page views, cart actions, checkout, purchase)  
- **sessions** – aggregated session information  
- **customers** – customer identifiers and high-level attributes  
- **orders** – purchase data  

Event data is processed into **feature-engineered tables** for analysis.

---

## Project Structure

```text
customer-behaviour-insight-engine/
├── data/
│   ├── raw/                # Original CSV data
│   └── processed/          # Feature-engineered tables
│
├── notebooks/
│   ├── 1_data_preparation.ipynb
│   ├── 2_session_enrichment.ipynb
│   ├── 3_behaviour_funnels.ipynb
│   ├── 4_path_analysis.ipynb
│   ├── 5_customer_metrics.ipynb
│   └── 6_association_analysis.ipynb
│
├── src/                    # Reusable helper functions (if applicable)
├── README.md
└── requirements.txt ```

---

## Analysis Steps

# 1. Data Preparation
	•	Load and clean raw CSV files
	•	Parse timestamps and identifiers
	•	Validate event sequences

# 2. Session Enrichment
	•	Aggregate events into session-level features
	•	Create funnel flags:
	•	page view
	•	add to cart
	•	checkout
	•	purchase
  •	Calculate session duration and revenue metrics

# 3. Behaviour Funnels
	•	Build multi-step funnels:
	•	View → Cart
	•	Cart → Checkout
	•	Checkout → Purchase
	•	Compute conversion and drop-off rates
	•	Segment funnels by:
	•	device
	•	country

# 4. Path Analysis
	•	Construct ordered session paths
	•	Identify most common navigation sequences
	•	Quantify path frequency and share of total sessions

# 5. Customer-Level Metrics
	•	Aggregate sessions per customer
	•	Analyse repeat behaviour and purchasing patterns
	•	Highlight differences between session-level and customer-level insights

# 6. Association Analysis (Apriori)
	•	Apply one-hot encoding and Apriori analysis
	•	Evaluate support, confidence, and lift
	•	Critically assess usefulness given low multi-item session frequency

## Tools & Technologies
	•	Python: Pandas, NumPy, Matplotlib
	•	SQL: PostgreSQL (via DBeaver)
	•	Notebooks: Jupyter
	•	Version Control: Git & GitHub

---
  
## What This Project Demonstrates
	•	Translating raw event data into meaningful analytics tables
	•	Structuring a multi-step analytics workflow
	•	Critical thinking about when certain methods are appropriate
	•	Communicating insights clearly through code, tables, and visuals
	•	A practical, business-oriented approach to behavioural data analysis

---

## Possible Extensions
	•	Customer-level sequence modelling across multiple sessions
	•	Markov chain or transition-based path analysis
	•	Product-level funnels
	•	Dashboarding (e.g. Tableau, Power BI)
	•	Cloud deployment (e.g. scheduled pipelines, database ingestion)


  






  
