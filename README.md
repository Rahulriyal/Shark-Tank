# Shark Tank India - Power BI Capstone Project

## 📌 Project Overview
This Power BI dashboard analyzes investment trends in **Shark Tank India**, providing insights into funding patterns, industry preferences, and investor behavior.

## 📊 Data Sources
- **Dataset**: Shark Tank India Investment Data
- **File Type**: CSV
- **Key Columns**: Startup Name, Industry, Investment Amount, Equity Percentage, Investor Names, Season, Deal Status

## 🔗 Data Model & Relationships
The data model consists of multiple tables linked via **primary-foreign key relationships**:
- **Startups Table** (Primary) → Connected to **Investments Table** via `Startup ID`
- **Investors Table** → Connected via `Investor ID`
- **Industry Table** → Connected via `Industry ID`

## 🧮 DAX Calculations
Several **DAX measures** are used for data analysis:
- **Total Investment**: `SUM(Investments[Investment Amount])`
- **Average Investment Per Deal**: `DIVIDE([Total Investment], COUNT(Investments[Deal ID]))`
- **Investor Contribution %**: `DIVIDE(SUM(Investments[Investment Amount]), [Total Investment]) * 100`
- **Equity % by Industry**: `AVERAGE(Investments[Equity Percentage])`

## 📈 Key Visualizations
The dashboard includes:
- **Total Funding by Industry** (Bar Chart)
- **Top Investors & Their Deals** (Table Visualization)
- **Investment Trends Over Seasons** (Line Chart)
- **Funding Distribution by Equity %** (Pie Chart)

## 📌 Insights & Business Impact
- **Technology & Consumer Goods** sectors received the highest funding.
- **Sharks like Aman Gupta & Peyush Bansal** made the most investments.
- **Average deal size increased in later seasons**, indicating growing investor confidence.
- **Most deals involved equity between 5% - 15%**, suggesting cautious investor strategies.

## 🚀 How to Use
1. Open **Power BI**
2. Load the `.pbix` file
3. Interact with visualizations & filters to explore insights

## 📜 License
MIT License - Open for public use and modifications.
