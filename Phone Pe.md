# 📊 PhonePe Transaction Insights

An end-to-end data analysis and visualization project focused on uncovering insights from PhonePe Pulse data, with a special emphasis on transaction trends, insurance penetration, user engagement, and device usage across India. The project uses **SQL, Python, Pandas, Matplotlib, Seaborn**, and **Streamlit** for dashboard development.

---

## 🧠 Project Objective

To extract, analyze, and visualize PhonePe transaction and insurance data to derive meaningful business insights that can guide:
- User engagement strategies
- Regional market expansion
- Insurance penetration optimization
- Transaction behavior analysis
- Dashboard-based storytelling for decision-makers

---

## 🔍 Problem Statement

With increasing reliance on digital payment platforms like PhonePe, it becomes essential to understand user behavior, transaction trends, and regional patterns. This project analyzes transaction categories, insurance growth, and top-performing regions to support data-driven business decisions and boost platform effectiveness.

---

## 📁 Dataset Source

The dataset is sourced from the [PhonePe Pulse GitHub Repository](https://github.com/PhonePe/pulse). It contains:
- Aggregated transaction, user, and insurance data
- Map-based summaries at state and district level
- Top performing categories, states, districts, and pincodes

---

## 🛠 Tech Stack

- **Python 3.11**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **SQLite3 / SQL**
- **Streamlit**
- **LocalTunnel** (for Streamlit deployment in Google Colab)

---

## 📊 Project Structure

### 1. Data Extraction & Loading
- Clone GitHub repo
- Extract and load JSON data into a SQL database (SQLite in-memory DB for Colab)

### 2. Exploratory Data Analysis (EDA)
- SQL queries for initial exploration
- Pandas-based DataFrames for aggregation and wrangling
- Charts to explore trends (Bar, Line, Heatmap, Pie)

### 3. Data Visualization & Storytelling
- Created 15+ charts showing:
  - Top states by transaction volume and insurance premium
  - App opens and user registration by brand
  - Quarterly trend charts
  - Correlation heatmap and pairplot

### 4. Hypothesis Testing
- Example hypotheses tested using t-test and ANOVA:
  - Does insurance penetration differ by state?
  - Are app opens significantly higher in some quarters?

### 5. Feature Engineering (Optional)
- Not used as the project was primarily EDA + Dashboard-based

### 6. Streamlit Dashboard
- Multi-tab Streamlit dashboard built with:
  - Sidebar navigation
  - Top performer insights
  - Transaction and insurance analytics
  - Time-series trends

---

## 📈 Key Business Use Cases

- 📌 **Top Performing Regions** – Identify states/districts for focused marketing
- 💼 **Insurance Analytics** – Understand growth patterns and market gaps
- 📱 **Device Usage Behavior** – Align UX with popular brands
- 📆 **Quarterly Trend Analysis** – Campaign planning based on seasonality
- 📊 **User Engagement** – Pinpoint high vs low engagement zones

---

## 🧪 Evaluation Metrics

| Metric                   | Description                                      |
|--------------------------|--------------------------------------------------|
| Code Quality             | Structured, modular code with SQL + Python      |
| SQL Query Efficiency     | Optimized queries for grouped operations        |
| Data Visualization       | Clear, color-contrasted visual storytelling     |
| Insights Validity        | Business-relevant and actionable insights       |
| Documentation Quality    | Full documentation of steps, methods, and logic|

---

## 📌 How to Run the Project (in Colab)

1. Clone the repo in Colab:
```python
!git clone https://github.com/PhonePe/pulse

Set up the database and load the tables using SQLite and Pandas.

To launch the dashboard:

bash
Copy
Edit
!pip install streamlit localtunnel
!streamlit run main.py & npx localtunnel --port 8501
Access the dashboard via the localtunnel link provided.

🧾 Business Case Studies Included
Transaction Analysis Across States and Districts

Device Dominance and User Engagement

Insurance Penetration and Growth Potential

User Registration Trends

Insurance Engagement Patterns

📌 Contributors
Unnimaya K – Data Analyst & Developer


