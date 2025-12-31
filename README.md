# 📊 Cross-Border Spend Monitoring (Power BI)

**Repo:** `pbi-green-bank-cross-border-spend-monitoring`

This repository contains a **Power BI demo solution** that models and visualises cross-border customer spend for a fictional retail bank, **Green Bank**.  
The focus is on **risk monitoring**, **annual limit breaches**, and **executive-level oversight**, using realistic financial services reporting patterns.

The project demonstrates **best-practice dimensional modelling**, **advanced DAX**, and **defensible KPI design**, with particular emphasis on correct evaluation grain and auditability.

---

## Installation Guide & Requirements

Please download the ZIP file and extract it to your preferred location.

You will need to have Power BI (version as at 29-12-2025) and a WIndows Operating System (Windows 11 or newer).



---

## 🔍 Business Objective

Provide a clear, auditable way to answer core risk and governance questions:

- How much are customers spending in total?
- How much of that spend is cross-border?
- Which customers are breaching annual spending limits?
- Where are risk controls failing (by branch, region, and channel)?

The solution is designed to support:
- Executive dashboards  
- Risk and compliance teams  
- Branch-level operational controls  

---

## 🧱 Data Model Highlights

- Star-schema design
- `FactTransaction` for individual spend events
- `FactNotification` for limit breach alerts
- Conformed dimensions:
  - Customer
  - Date
  - Branch
  - Country
  - Channel
- Clear separation of:
  - Transaction-level grain
  - Customer–year risk grain
- Clean, single-direction relationships for predictable filtering and performance

---

## 🧮 DAX & Analytics

- Cumulative annual spend calculations per customer
- Annual limit breach detection using context-aware measures
- Correct handling of evaluation grain (customer-year vs transaction-day)
- Defensive DAX patterns to avoid:
  - Inflated totals
  - Misleading aggregations
  - Incorrect visual interpretation

This project intentionally demonstrates why **some measures should only be evaluated at specific grains**, a common and costly pitfall in real-world Power BI models.

---

## 📄 Report Pages

### 1. Executive Overview
- Total Spend (GBP)
- Cross-Border Spend (GBP)
- % Cross-Border Spend
- Customers Over Limit
- Date and Branch slicers

### 2. Customer Risk
- Customer-level breach analysis
- Annual spend vs limit comparison
- Branch and destination country filtering

### 3. Breach Control Monitoring
- Breaches by Year, Channel, Region (Origin & Destination) and Customer
- Breach Notifications (Type and Volume)
- Detailed Customer level breach table for auditability

---

## 🎯 Intended Audience

- Power BI developers
- Analytics engineers
- Risk & compliance analysts
- Hiring managers reviewing realistic Power BI work samples

---

## 🛠 Tools & Technologies

- Power BI Desktop
- DAX
- Dimensional modelling (Kimball-style)
- Financial risk and control reporting patterns
- AI for synthetic data and logo generation (ChatGPT 5.2)
- Google search for colour palette inspiration
- JSON for custom Power BI theme

---

## ⚠️ Disclaimer

All data, entities, and scenarios in this repository are **entirely fictional** and provided for **demonstration purposes only**.  
They do not represent any real bank, customer, or financial activity.
