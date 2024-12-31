# Analysis of Industries Contributing to Virginia's GDP

## Overview
This project investigates the contributions of various industries to Virginia's GDP, aiming to identify key sectors for policy-making and economic investments. Using statistical and machine learning tools, the analysis provides insights into significant predictors of GDP at both sectoral and temporal levels.

We got the "𝐁𝐞𝐬𝐭 𝐏𝐫𝐞𝐬𝐞𝐧𝐭𝐚𝐭𝐢𝐨𝐧 𝐟𝐨𝐫 𝐚 𝐍𝐨𝐧-𝐓𝐞𝐜𝐡𝐧𝐢𝐜𝐚𝐥 𝐀𝐮𝐝𝐢𝐞𝐧𝐜𝐞 𝐚𝐰𝐚𝐫𝐝!🏆"
https://www.linkedin.com/feed/update/urn:li:activity:7279590895132246016/

## Features
- **Data Import and Cleaning**: Processes GDP data categorized by sector and year.
- **Exploratory Data Analysis (EDA)**: Visualizes trends, identifies outliers, and evaluates data distributions.
- **Feature Engineering**: Transforms temporal and sectoral variables for better modeling.
- **Model Development**: Builds and evaluates linear models to identify significant sectors.
- **Interpretability Focus**: Prioritizes simple models to maintain clarity in findings.

## Key Findings
- Sectors like **Government** and **Real Estate** have high positive coefficients, indicating strong positive contributions to GDP.
- Sectors like **Education** and **Mining** show negative coefficients, reflecting an inverse relationship with GDP.
- Including interaction effects (e.g., sector and year) did not significantly improve model interpretability or predictive power.

## Installation
Ensure the following R packages are installed:

```R
install.packages(c("MASS", "car", "lmtest", "mltools", "forecast"))
```

Usage
Data Import and Visualization
Load the data:
R
Copy code
data <- read.csv("ML_gdp_data.csv", stringsAsFactors = TRUE)
Perform exploratory visualizations:
R
Copy code
plot(GDP ~ Sector, data = data)
hist(data$GDP)
Model Building
Fit a simple linear model:
R
Copy code
model1 <- lm(GDP ~ Sector, data = data)
summary(model1)
Evaluate interaction effects (optional):
R
Copy code
model2 <- lm(GDP ~ Sector * Year, data = data)
summary(model2)
Results Interpretation
The linear model without interaction effects proved sufficient for deriving insights into sector-level GDP contributions, with clear beta coefficients indicating proportional relationships.

Data Insights
Government and Real Estate: High positive impact.
Education and Mining: Negative impact.
Temporal Trends: Sector contributions varied by quarter during economic disruptions like 2020 (e.g., COVID-19 effects on Real Estate and Leasing).
Future Work
Normalization: Explore transformations (e.g., log scale) for variables like GDP.
Sector-Specific Analysis: Deep dive into key industries, e.g., Real Estate and Government.
Temporal Models: Incorporate advanced time-series analysis to capture dynamic trends.
Contributions
This analysis serves as a foundation for policymakers and economists to prioritize investments in Virginia's most impactful sectors.

