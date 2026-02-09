# 📈 Marketing Spend Optimization & ROI Analysis

**Role Focus:** Data Strategy | Marketing Analytics | Business Intelligence
**Tech Stack:** Python, Scikit-Learn, Pandas, Multiple Linear Regression

## 1. The Business Strategy (The "Why")
**Objective:** To quantify the impact of multi-channel marketing spend on total revenue and identify which channels provide the highest marginal return on investment (ROI).
* **Business Problem:** Marketing budgets were allocated based on intuition rather than data. The goal was to replace guesswork with a statistical model to determine **Marketing Efficiency** (Revenue per unit of spend).
* **Strategic Outcome:** By identifying the "Marketing Efficiency" coefficient for Social Media vs. TV, the business can reallocate budget from low-performing channels to high-performing ones to maximize total profit.

## 2. Technical Methodology (The "How")
* **Feature Engineering:** Created a custom metric for **Marketing Efficiency Ratio (MER)**: $\text{Revenue} / \text{Total Spend}$.
* **Predictive Modeling:** Utilized **Multiple Linear Regression** to estimate the coefficients for each marketing channel.
* **Statistical Validation:** Analyzed the **Coefficient of Determination ($R^2$)** to evaluate how much revenue variance is explained by marketing activities vs. external factors.

## 3. Business Intelligence & Insights (The "View")
* **EDA:** Generated correlation heatmaps to identify which channels move in lockstep with revenue.
* **Key Insight:** Discovered that while TV Spend had high visibility, **Digital Spend** had a significantly higher marginal coefficient, suggesting a strategy shift toward digital channels.
* **Actionable Recommendation:** Proposed a budget reallocation plan to prioritize channels where a $1 increase in spend results in the highest predicted revenue increase.


---

# 🚑 Traffic Accident Severity & Casualty Prediction

**Role Focus:** Public Policy Analyst | Risk Manager | Data Scientist
**Tech Stack:** Python, Scikit-Learn (Random Forest), Pandas, Imbalanced Data Handling

## 1. The Business Strategy (The "Why")
**Objective:** To move from reactive accident reporting to **proactive risk management** by predicting the severity of traffic accidents based on environmental factors.
* **Social Impact:** By identifying high-risk conditions (e.g., specific times, weather patterns), governments can allocate emergency resources effectively to reduce fatalities.
* **Strategic Goal:** Deploy warning systems in high-risk zones to lower the casualty rate during predicted "danger windows."

## 2. Technical Methodology (The "How")
* **Handling Imbalanced Data:** Addressed the "Accuracy Paradox" (few fatal accidents vs. many minor ones) by optimizing for **Recall** to minimize False Negatives (missed fatal predictions).
* **Feature Engineering:** Converted raw timestamps into cyclical features (Rush Hour patterns) to capture temporal risk.
* **Model Selection:** Benchmarked **Logistic Regression** (for interpretability) against **Random Forest** (for non-linear accuracy), finding that Random Forest offered superior F1-Scores.

## 3. Insights & Recommendations (The "Strategy")
* **Critical Risk Factors:** The model revealed that **Time of Day** and **Lighting Conditions** (specifically Twilight) were top predictors of severity—more so than vehicle type.
* **Policy Recommendation:** Proposed increasing street lighting in specific zones and pre-positioning EMS units near high-risk intersections during Friday evening rush hours.



---
