# Analysis of the Relationship Between Population Growth and CPI in Sweden (2010–2024)  
**Author:** Yoshihiro Tsunoda  
**Date:** 21/11/2025  

---

## Technical Environment
- **Python 3.12**
- **Libraries:** pandas, matplotlib, seaborn, scikit-learn
- **Data Source:** Statistics Sweden (SCB)
- **Visualizations:**
  - Line charts  
  - Scatter plots  
  - Regression line
- **Methods:**
  - Year-over-year percentage change calculation
  - Simple linear regression

---

## Abstract
This report analyzes the relationship between annual population growth and Consumer Price Index (CPI) changes in Sweden from 2010 to 2024 using publicly available SCB data. Visual inspection and linear regression suggest a weak negative correlation between the two indicators. While CPI growth may slightly coincide with slower population growth in some years, CPI alone is insufficient to explain national demographic trends.

---

## 1. Introduction
Population growth is influenced by a wide range of factors such as fertility rates, immigration, employment, and public policy. Inflation, reflected in CPI, affects household living costs and may influence demographic behavior.

This report examines whether fluctuations in CPI show a measurable impact on Sweden’s annual population growth using time-series visualization and regression analysis.

---

## 2. Data and Methods

### 2.1 Data
- **Population Data (SCB):** Annual regional population statistics from SCB
  - Columns: `Year`, `Region`, `Population`
  - Format: Long (tidy) format

- **CPI Data (SCB):** Annual national Consumer Price Index from SCB
  - Columns: `Year`, `CPI`
  - Regional CPI data not available

- **Time Period:** 2010–2024

### 2.2 Methodology

1. Aggregate the total national population per year.  
2. Compute year-over-year percentage changes:
      pop_growth_rate = Population.pct_change() * 100
      cpi_growth_rate = CPI.pct_change() * 100
3. Merge population and CPI datasets by year.
4. Create visualizations:
    - National population trend (2010–2024)
    - National CPI trend (2010–2024)
    - Comparison of population and CPI growth rates (time series)
    - Scatter plot of population vs CPI growth
    - Regression plot with fitted line
5. Perform a simple linear regression using:
    - **Explanatory variable (X):** CPI growth rate  
    - **Response variable (Y):** Population growth rate

---

## 3. Results

### 3.1 National Population Trend (2010–2024)
**Figure 1. National population growth in Sweden (2010–2024)**

Sweden’s population increased steadily from approximately **9.4 million** in 2010 to **10.6 million** in 2024. Although the population grows every year, the pace of growth gradually slows over the period.

---

### 3.2 National CPI Trend (2010–2024)
**Figure 2. Swedish CPI trend (2010–2024)**

CPI rises from around **308** in 2010 to **41**7 in 2024. Growth remained moderate—typically below **2%** annually—until 2020. Sharp increases occurred from 2020 to 2022, reaching a peak of **+12%** in 2022 before stabilizing.

---

### 3.3 Comparison of Population and CPI Growth Rates (2010–2024)
**Figure 3. Population growth vs CPI growth compaared (time series)**

Key observations:

- 2010–2016: Population growth consistently around **+1%**
- 2020–2022: CPI surges sharply while population growth remains flat
- After 2022: CPI declines but population growth does not rebound immediately

This suggests a possible relationship where higher inflation aligns with slower population expansion, although causality cannot be assumed.
---

### 3.4 Scatter Plot of Population Growth vs CPI Growth
**Figure 4. Scatter plot of CPI vs population growth**

The data shows no strong linear pattern.   
The correlation coefficient is:

    **r ≈ –0.25**

This indicates a **weak negative correlation**, meaning:

- Higher CPI tends to coincide with slightly lower population growth
- But the relationship is not strong enough to explain demographic variation on its own

---

### 3.5 Regression Analysis (CPI → Population Growth)
**Figure 5. Regression line fitted on CPI and population growth**

- Regression coefficient: **–0.026**  
- R²: **0.064**

Interpretation:

- The negative coefficient means population growth tends to decline very slightly when CPI increases
- But the **R² value of 6% shows that CPI explains only a small portion of population variation**
- Other demographic forces (immigration, fertility, economic conditions, policy, housing costs) likely have stronger effects

---

## 4. Discussion
- CPI and population growth display a weak inverse relationship
- The low R² indicates that most population variation is driven by other factors
- Even during the rapid price increases of 2020–2022, population growth showed minimal movement
- CPI may play a role, but is not a primary driver of demographic change in Sweden

---

## 5. Conclusion
Key findings:

- CPI growth alone does not sufficiently explain national population change (R² ≈ 0.06)
- For meaningful demographic forecasting, additional variables are needed, such as:
  - Immigration flows
  - Fertility rates
  - Labor market conditions
  - Housing policy
  - Broader economic indicators

This study serves as exploratory analysis; multivariate modeling could further clarify underlying relationships.

---

## 6. References
- Statistics Sweden (SCB). Population Statistics  
- Statistics Sweden (SCB). Consumer Price Index (CPI)  
- Seaborn Documentation  
- scikit-learn Documentation
