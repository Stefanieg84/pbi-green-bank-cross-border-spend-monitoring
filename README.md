# 📊 Cross-Border Spend Monitoring (Power BI)

**Repo:** `pbi-green-bank-cross-border-spend-monitoring`

This repository contains a **Power BI demo solution** that models and visualises cross-border customer spend for a fictional retail bank, **Green Bank**.  
The focus is on **risk monitoring**, **annual limit breaches**, and **executive-level oversight**, using realistic financial services reporting patterns.

The project demonstrates **best-practice dimensional modelling**, **advanced DAX**, and **defensible KPI design**, with particular emphasis on correct evaluation grain and auditability.

---
## Preview Screenshots

![Executive Overview](<screenshot_previews/Green Bank Dashboard Page 1 - Executive Overview.jpeg>) ![Customer Risk](<screenshot_previews/Green Bank Dashboard Page 2 - Customer Risk.jpeg>) ![Breach Control Effectiveness](<screenshot_previews/Green Bank Dashboard Page 3 - Breach Control Effectiveness.jpeg>) ![Q&A](<screenshot_previews/Green Bank Dashboard Page 4 - Q&A.jpeg>)

---

## Installation Guide & Requirements

Please download the ZIP file and extract it to your preferred location on your local device.

You will need to have Power BI (version as at 29-12-2025) and a Windows Operating System (Windows 11 or newer).

I wanted to share a live link, but this is not an option as I do not have the premium organisation license.

You should be able to review the full dashboard (including data model, DAX measures and Power Query steps) on your local windows desktop.

For the best experience, and if this is suitable for you, you can publish the dashboard to your private organisation workspace, given that you have a Power BI license (or trial).

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
