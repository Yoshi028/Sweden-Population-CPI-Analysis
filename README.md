# Sweden-Population-CPI-Analysis

This repository contains a data analysis project examining the relationship between
population growth and inflation (CPI increase rate) from 2010 to 2024.

## 📌 Objectives
- Analyze trends in population growth and CPI change over time
- Investigate whether inflation correlates with population change
- Produce visualizations and regression analysis results
- Summarize insights in a structured research report

## 📊 Dataset
- Source: Statistics Sweden (SCB) 
- Period: 2010–2024  
- Variables used:
  - CPI growth rate (%)
  - Population growth rate (%)

## 🔍 Methods
- Yearly trend analysis
- Scatter plot comparison
- Simple linear regression  
  - Explanatory variable: CPI growth rate
  - Target variable: Population growth rate
- Visualization using Python (pandas, matplotlib, seaborn)

## 📈 Key Results (Summary)
- CPI varies widely year-to-year, ranging roughly from –0.3% to +12%
- Population growth rate fluctuates around 1% annually
- The correlation coefficient between CPI and population growth is around **–0.25**,  
  indicating a weak negative relationship
- Regression analysis suggests that higher inflation may be associated with lower population growth,  
  but the relationship is not strong

## 🧾 Contents
project/  
│  
├── data/ ← Raw and processed datasets  
├── output/ ← Generated charts (PNG)  
├── report/ ← Full written report (PDF)  
└── scripts/ ← Analysis scripts

## 📁 Available Visualizations  
Population growth trend (2010–2024)  
CPI growth trend (2010–2024)  
Population Growth Rate vs CPI Growth Rate (2010–2024)  
Scatter plot: CPI vs population growth  
Regression plot (with regression line)  

## 📚 Requirements
Python 3.9+  
pandas  
seaborn  
matplotlib  

## ✍ Author  
Yoshihiro Tsunoda  
2025-11-22

## 📄 License  
MIT License
