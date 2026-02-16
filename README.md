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

# ✈️ Airline Flight Delay Prediction & Cause Analysis

**Role Focus:** Data Scientist (Operations) | BI Analyst | Logistics Analyst
**Tech Stack:** Python, XGBoost, Scikit-Learn (Random Forest), Pandas, Feature Engineering

## 1. The Business Strategy (The "Why")
**Objective:** To mitigate the financial impact of flight delays by building a predictive engine that estimates arrival delays (`ArrDelay`) based on schedule and route data.
* **Business Problem:** Flight delays cause cascading operational bottlenecks, costing airlines billions in crew overtime, gate fees, and passenger compensation.
* **Strategic Goal:** Enable **Proactive Resource Management**. By predicting delay severity before takeoff, airlines can optimize gate assignments and adjust crew schedules to minimize downstream disruptions.

## 2. Technical Methodology (The "How")
* **Feature Engineering:**
    * **Temporal Binning:** Transformed raw timestamps into "Time-of-Day" bins (Morning, Afternoon, Evening) to capture congestion patterns.
    * **Seasonality:** Mapped flight dates to seasons to account for weather-related probability.
    * **Route Analytics:** Created interaction features (e.g., `Airline_Route`) to capture carrier-specific performance on specific corridors.
* **Model Selection:** Deployed **Ensemble Learning** techniques (**XGBoost Regressor** and **Random Forest**) to handle non-linear relationships between time, route, and delay magnitude.
* **Evaluation:** Optimized for **RMSE (Root Mean Squared Error)** to penalize large prediction errors that disrupt operations most.

## 3. Key Analysis Areas (The "View")
* **Operational Pattern Recognition:** Analyzed "Day of Week" and "Departure Hour" to identify peak congestion windows where delays are systemically higher.
* **Driver Analysis:** Investigated the correlation between **Distance Groups** and delay frequency (e.g., short-haul vs. long-haul turnover risks).
* **Outlier Detection:** Utilized statistical methods to identify and handle extreme weather events that could skew model training.

## 4. Business Insights & Strategic Recommendations (The "Strategy")
* **Schedule Buffering:** The analysis revealed that **Evening Flights** suffer from cascading delays accumulated throughout the day.
    * **Recommendation:** Increase "turnaround buffer time" for flights departing after 5:00 PM to absorb upstream variances without disrupting the network.
* **Route Optimization:** Specific corridors (e.g., High-Traffic Hubs) showed consistent delays regardless of weather.
    * **Recommendation:** Adjust block times (scheduled duration) for these specific routes to reflect reality, improving "On-Time Performance" (OTP) metrics reported to the DOT.
* **Proactive Crew Management:** High-probability delay warnings from the XGBoost model can trigger early crew re-assignment.
    * **Recommendation:** Deploy the model to Operations Control Centers (OCC) to flag "At-Risk" flights 4 hours out, preventing crew "timeout" (legal duty limit) cancellations.
