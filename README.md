# 🌾 Seasonal Agriculture Performance Analysis

### A Data-Driven Study of Seasonal Agricultural Performance, Resource Efficiency, Profitability, and Risk

**Author:** Tharun Pranav T

---

## 📌 Project Overview

Agricultural performance varies across seasons due to differences in environmental conditions, farming practices, resource availability, crop characteristics, and market conditions.

This project, **Seasonal Agriculture Performance Analysis**, presents a comprehensive data-driven analysis of farm-level agricultural data to understand how seasonal conditions influence agricultural productivity, resource efficiency, economic performance, and disease/pest risk.

The project uses exploratory data analysis, statistical analysis, visualization, correlation analysis, and comparative techniques to identify meaningful seasonal patterns and generate practical agricultural insights.

The analysis follows the overall flow:

**Seasonal Conditions → Agricultural Performance → Crop Response → Resource Efficiency → Economic Performance → Risk → Statistical Validation → Recommendations**

---

## 🎯 Problem Statement

Agricultural activities and outcomes can vary significantly between seasons because of changes in rainfall, temperature, humidity, soil moisture, irrigation requirements, crop characteristics, resource usage, market prices, and production costs.

Without systematic analysis, it can be difficult to determine:

- Which seasons demonstrate stronger agricultural performance
- How environmental conditions differ across seasons
- How crop productivity changes across seasons
- Which crops demonstrate stronger economic performance
- How irrigation methods perform under different seasonal conditions
- How efficiently water resources are being used
- How disease and pest risk varies seasonally
- Whether observed seasonal differences are statistically significant
- Which factors should be considered when making agricultural decisions

This project addresses these challenges by analyzing agricultural data across multiple dimensions and translating the results into data-driven insights and recommendations.

---

## 🎯 Objectives

The major objectives of this project are:

1. Explore and understand the agricultural dataset.
2. Clean and prepare the data for analysis.
3. Analyze environmental conditions across agricultural seasons.
4. Compare agricultural performance across Kharif, Rabi, and Zaid seasons.
5. Study crop-level performance across seasons.
6. Analyze irrigation methods and their observed performance.
7. Evaluate water usage and water efficiency.
8. Investigate relationships between environmental conditions and agricultural outcomes.
9. Analyze revenue, production cost, profit, and profitability.
10. Examine disease and pest risk across seasons and crops.
11. Identify statistically significant seasonal differences.
12. Use effect-size analysis to distinguish statistical significance from practical magnitude.
13. Identify important patterns, variations, and unusual observations.
14. Develop data-driven recommendations for agricultural planning.
15. Identify opportunities for future predictive analytics and intelligent agricultural decision-support systems.

---

## ❓ Key Analytical Questions

The project investigates questions such as:

- Which season demonstrates the strongest overall agricultural performance?
- How do rainfall, temperature, humidity, and soil moisture vary across seasons?
- How does crop yield change from one season to another?
- Do different crops respond differently to seasonal conditions?
- Which crops demonstrate stronger profitability?
- How does irrigation performance vary across seasons?
- How efficiently is water being converted into agricultural output?
- What relationships exist between environmental variables and agricultural outcomes?
- How does disease/pest risk vary across seasons?
- How are revenue, cost, and profit affected by seasonal conditions?
- Are the observed seasonal differences statistically significant?
- Which agricultural indicators show stronger practical seasonal effects?
- What factors should be considered when planning agricultural activities?

---

# 📊 Dataset

The dataset contains **4,000 observations and 28 variables** representing farm-level agricultural, environmental, resource, economic, and risk-related information. :contentReference[oaicite:1]{index=1}

## Dataset Summary

| Attribute | Value |
|---|---:|
| Total Records | 4,000 |
| Total Variables | 28 |
| Seasons | 3 |
| Crops | 8 |
| States | 8 |
| Districts | 10 |
| Irrigation Methods | 4 |

### Seasons

- Kharif
- Rabi
- Zaid

### Crops

- Wheat
- Maize
- Pulses
- Rice
- Cotton
- Chilli
- Groundnut
- Sugarcane

### Irrigation Methods

- Drip
- Flood
- Rainfed
- Sprinkler

---

# 📋 Dataset Variables

## Farm Information

- `Farm_ID`
- `State`
- `District`
- `Crop`
- `Season`
- `Farm_Area_Hectares`

## Environmental Conditions

- `Rainfall_mm`
- `Avg_Temperature_C`
- `Humidity_pct`
- `Sunlight_Hours_Day`
- `Soil_pH`
- `Soil_Moisture_pct`

## Resource Usage

- `Nitrogen_kg_ha`
- `Phosphorus_kg_ha`
- `Potassium_kg_ha`
- `Irrigation_Method`
- `Fertilizer_kg_ha`
- `Pesticide_Litre_ha`
- `Seed_Quality_Score`

## Agricultural Performance

- `Yield_Tonnes_Ha`
- `Production_Tonnes`

## Economic Indicators

- `Market_Price_INR_Tonne`
- `Total_Cost_INR`
- `Revenue_INR`
- `Profit_INR`

## Resource Efficiency and Risk

- `Water_Used_m3`
- `Water_Efficiency_t_per_1000m3`
- `Disease_Pest_Risk_pct`

---

# 🧹 Data Preparation

The dataset was systematically examined for:

- Missing values
- Duplicate records
- Data types
- Category consistency
- Numerical ranges
- Distribution characteristics
- Extreme observations and potential outliers

## Missing Values

Missing values were identified in selected variables, including:

- Rainfall
- Soil moisture
- Yield

Rainfall and soil-moisture values were handled using **seasonal median imputation**.

Yield was treated differently because it is a primary agricultural performance outcome. Missing yield observations were not blindly imputed and were excluded from analyses requiring valid yield values.

## Duplicate Records

Duplicate records were checked during data preparation.

## Outlier Treatment

Extreme observations were not automatically removed because they may represent genuine agricultural conditions.

Robust statistical measures such as **medians** and non-parametric statistical tests were therefore used for important comparisons.

## Crop Scale Consideration

Crop yield values have substantially different scales.

Sugarcane, in particular, has a much higher tonnes-per-hectare scale than several other crops.

Therefore, crop-specific comparisons and sensitivity analysis excluding Sugarcane were used where appropriate rather than treating all raw yield values as directly comparable.

---

# ⚙️ Feature Engineering

Additional analytical variables were created to support normalized economic and performance comparisons.

## Derived Features

| Feature | Purpose |
|---|---|
| `Revenue_per_Ha` | Revenue normalized by farm area |
| `Profit_per_Ha` | Profit normalized by farm area |
| `Profit_Margin_pct` | Profit as a percentage of revenue |
| `Cost_per_Tonne` | Production cost relative to output |
| `Revenue_per_Tonne` | Revenue relative to output |
| `Loss_Making` | Identifies observations with negative profit |

These derived indicators provide a more meaningful basis for comparing farms with different production scales.

---

# 📈 Exploratory Data Analysis

The exploratory analysis covers the following areas:

- Seasonal distribution
- Environmental conditions
- Crop distribution
- Irrigation distribution
- Seasonal crop composition
- Rainfall
- Temperature
- Humidity
- Soil moisture
- Yield
- Water efficiency
- Disease/pest risk
- Crop-season performance
- Crop resilience
- Irrigation performance
- Water usage
- Environmental relationships
- Revenue
- Production cost
- Profit
- Profit margin
- Loss-making farms
- Crop profitability

---

# 🌦️ Seasonal Environmental Analysis

The analysis identifies substantial differences in environmental conditions across seasons.

Kharif generally records higher rainfall, humidity, and soil moisture compared with Rabi and Zaid.

These environmental differences provide important context when interpreting changes in agricultural productivity, resource efficiency, and economic outcomes.

---

# 🌾 Seasonal Performance Findings

The analysis identifies clear differences in agricultural performance across seasons.

## Kharif

Kharif demonstrates comparatively stronger overall performance, including:

- Higher median yield
- Higher median water efficiency
- Positive median profit
- Lower proportion of loss-making farms compared with later seasons

## Rabi

Rabi generally records intermediate performance between Kharif and Zaid.

## Zaid

Zaid records comparatively weaker:

- Median yield
- Water efficiency
- Profitability

It also has a higher proportion of loss-making observations.

Overall, the analysis indicates a progressive decline in several important agricultural performance indicators from:

**Kharif → Rabi → Zaid**

---

# 🌱 Crop-Level Findings

The crop-season analysis shows that seasonal performance differs across crops.

All eight crops in the dataset show a decline in median yield from Kharif to Rabi and from Rabi to Zaid.

However, the magnitude of seasonal change differs by crop.

This demonstrates that seasonal agricultural planning should consider **crop-specific responses** rather than applying a single strategy to every crop.

---

# 💰 Crop Profitability Findings

Crop profitability varies considerably across seasons.

**Chilli and Sugarcane** demonstrate comparatively stronger profit per hectare across the analyzed seasons.

Several other crops show weaker or negative profitability during Rabi and Zaid.

These findings indicate that crop selection should consider both:

**Expected Productivity + Expected Profitability**

rather than yield alone.

These findings should be interpreted within the environmental and market conditions represented by the dataset and should not be treated as guaranteed future returns.

---

# 💧 Irrigation Findings

The irrigation analysis indicates that irrigation performance varies by season.

Observed median yield patterns show:

- **Drip** performing strongly during Kharif and Rabi.
- **Sprinkler** recording the highest median yield among irrigation methods during Zaid.

These are observational findings and should not be interpreted as proof that one irrigation method directly causes higher yield.

Irrigation decisions should consider:

- Season
- Crop requirements
- Water availability
- Water efficiency
- Environmental conditions

---

# 💦 Water Efficiency Findings

Water efficiency varies across seasons and irrigation methods.

Therefore, water consumption should not be evaluated independently.

A more useful assessment considers:

**Water Used + Agricultural Output → Water Efficiency**

This provides a more meaningful perspective on resource productivity.

---

# ⚠️ Disease and Pest Risk Findings

Disease and pest risk shows substantial seasonal variation.

Kharif records the highest median reported disease/pest risk among the three seasons.

Risk also differs across crops.

The analysis therefore highlights the importance of considering disease and pest risk as part of seasonal agricultural planning.

---

# 🔗 Environmental Relationships

Spearman rank correlation was used to investigate relationships between:

- Rainfall
- Temperature
- Humidity
- Soil moisture
- Resource usage
- Yield
- Water efficiency
- Profitability
- Disease/pest risk

Correlation results indicate observed associations between selected variables.

These relationships should not be interpreted as causal effects because the dataset is observational.

---

# 🧪 Pesticide Usage and Disease/Pest Risk

The analysis identifies a negative observational association between pesticide usage and reported disease/pest risk.

However, this does **not** establish that increased pesticide usage directly reduces disease or pest risk.

Other factors may influence both pesticide usage and reported risk, including:

- Environmental conditions
- Crop characteristics
- Existing risk levels
- Farming practices
- Management decisions

Therefore, this relationship should be treated as an observational finding requiring further investigation.

---

# 📊 Statistical Analysis

Statistical tests were applied to validate important patterns identified during exploratory analysis.

## Kruskal-Wallis Test

The Kruskal-Wallis test was used to compare the distributions of selected agricultural indicators across:

- Kharif
- Rabi
- Zaid

The test was applied to:

- Yield
- Profit
- Water efficiency
- Disease/pest risk

## Mann-Whitney U Test

Pairwise comparisons were performed for:

- Kharif vs Rabi
- Kharif vs Zaid
- Rabi vs Zaid

## Bonferroni Correction

Bonferroni correction was applied to control for multiple pairwise comparisons.

## Spearman Correlation

Spearman rank correlation was used to examine monotonic relationships between environmental, resource, performance, economic, and risk variables.

## Chi-Square Test

Chi-Square testing was used to investigate associations between season and categorical variables such as:

- Crop
- Irrigation method
- State
- District

## Effect Size

Epsilon-squared was used alongside Kruskal-Wallis testing to distinguish statistical significance from practical magnitude.

---

# 📐 Statistical Evidence

The Kruskal-Wallis analysis indicates statistically significant seasonal differences in:

- Yield
- Profit
- Water efficiency
- Disease/pest risk

The effect-size analysis shows that these statistically significant differences do not all have the same practical magnitude.

Disease/pest risk demonstrates a comparatively stronger seasonal effect than the other tested indicators.

This highlights the importance of evaluating both:

**Statistical Significance + Practical Effect Size**

rather than relying only on p-values.

---

# 🔍 Key Findings

## Finding 1 — Kharif Shows Stronger Overall Performance

Kharif records comparatively higher median yield, water efficiency, and profit per hectare.

## Finding 2 — Performance Declines Across Seasons

Median yield decreases from Kharif to Rabi and further to Zaid.

## Finding 3 — Economic Vulnerability Increases

Rabi and Zaid demonstrate weaker profitability, while the proportion of loss-making observations increases across seasons.

## Finding 4 — Environmental Conditions Differ Strongly

Rainfall, humidity, soil moisture, and temperature vary substantially between seasons.

## Finding 5 — Crop Response Is Not Uniform

All analyzed crops show declining median yield across seasons, but the magnitude of decline varies by crop.

## Finding 6 — Chilli and Sugarcane Show Stronger Profitability

These crops demonstrate comparatively stronger profit per hectare across the analyzed seasons.

## Finding 7 — Irrigation Performance Is Seasonal

Observed irrigation performance varies between seasons, indicating the importance of evaluating irrigation within its seasonal context.

## Finding 8 — Disease/Pest Risk Is Strongly Seasonal

Kharif records the highest median reported disease/pest risk.

## Finding 9 — Statistical Tests Support Important Seasonal Differences

Kruskal-Wallis analysis indicates statistically significant differences in yield, profit, water efficiency, and disease/pest risk across seasons.

## Finding 10 — Correlation Does Not Imply Causation

Observed relationships should be interpreted as associations rather than direct causal effects.

---

# 💡 Data-Driven Recommendations

## Seasonal Planning

- Use seasonal environmental and historical performance indicators when planning agricultural activities.
- Evaluate profitability carefully during Rabi and Zaid.
- Consider rainfall, temperature, humidity, and soil moisture alongside agricultural performance.

## Crop Selection

- Evaluate crops using both yield and profitability.
- Consider crop-specific seasonal performance.
- Give greater attention to crops demonstrating comparatively stable economic performance where environmental and market conditions are suitable.

## Irrigation

- Select irrigation methods according to seasonal conditions and crop requirements.
- Evaluate irrigation using both yield and water efficiency.
- Monitor irrigation performance separately across seasons.

## Resource Efficiency

- Monitor water consumption relative to agricultural output.
- Track water efficiency at crop and seasonal levels.
- Consider resource efficiency when comparing alternative crop-season strategies.

## Economic Planning

- Evaluate expected revenue, cost, and profit before committing resources.
- Use profit per hectare when comparing farms with different sizes.
- Consider market price and production cost alongside yield.

## Disease and Pest Management

- Strengthen monitoring during higher-risk seasonal periods.
- Use crop-specific risk patterns for preventive planning.
- Consider environmental conditions when monitoring disease and pest risk.
- Treat pesticide-risk relationships as observational indicators rather than causal evidence.

---

# 🧠 Data-Driven Decision Framework

The project proposes evaluating agricultural decisions using multiple dimensions:

**Environmental Conditions  
+ Crop Performance  
+ Irrigation  
+ Resource Efficiency  
+ Profitability  
+ Risk  
↓  
Seasonal Agricultural Decision**

This multi-factor approach is more informative than evaluating agricultural performance using yield alone.

---

# ⚠️ Limitations

## Observational Dataset

The dataset represents observed agricultural conditions and outcomes. Therefore, statistical relationships cannot establish causal relationships.

## Missing Values

Selected variables contain missing observations. Appropriate treatment methods were applied, but imputation may introduce some uncertainty.

## Differences in Crop Scale

Crop yield scales differ substantially, particularly for Sugarcane.

Therefore, raw yield values should not be interpreted as directly comparable across all crops.

## Outliers and Skewed Distributions

Variables such as yield, production, revenue, and profit contain skewed distributions and extreme observations.

These observations were not automatically removed because they may represent genuine agricultural conditions.

## Geographic Coverage

The dataset covers a limited number of states and districts.

Therefore, findings should not automatically be generalized to all agricultural regions.

## Lack of Explicit Year-Level Time Series

The dataset contains seasonal information but does not provide a detailed year-by-year time-series structure.

Therefore, the analysis focuses on seasonal differences rather than long-term agricultural or climate trends.

## Market Variability

Future market prices and production costs may differ from those represented in the dataset.

Profitability findings should therefore be treated as historical evidence rather than guaranteed future returns.

## No Causal Inference

The statistical methods used identify differences and associations but do not establish causal mechanisms.

---

# 🚀 Future Scope

The current project can be extended into a comprehensive agricultural decision-support platform.

## 1. Larger and More Diverse Datasets

Future versions can incorporate additional:

- States
- Districts
- Crops
- Farming systems
- Historical observations

## 2. Real-Time Weather Integration

Real-time and historical weather information could be integrated to provide updated information on:

- Rainfall
- Temperature
- Humidity
- Soil moisture
- Other environmental conditions

## 3. Satellite and Remote-Sensing Data

Satellite imagery and remote-sensing indicators could provide additional information about:

- Crop health
- Vegetation
- Soil moisture
- Land conditions

## 4. Predictive Machine Learning

Future versions could develop models for predicting:

- Crop yield
- Profitability
- Water requirements
- Disease/pest risk
- Loss probability

## 5. Crop-Specific Prediction

Separate models could be developed for individual crops to account for their different yield scales, resource requirements, and environmental responses.

## 6. Risk Forecasting

Historical environmental and agricultural information could be used to develop predictive disease and pest risk forecasting systems.

## 7. Interactive Dashboard

The analysis could be transformed into an interactive dashboard using technologies such as:

- Power BI
- Tableau
- Streamlit

Users could explore results by:

- State
- District
- Crop
- Season
- Irrigation method

## 8. Intelligent Recommendation Engine

A future recommendation system could combine:

**Historical Data  
+ Weather Data  
+ Market Data  
+ Predictive Models  
+ Risk Assessment  
↓  
Intelligent Agricultural Recommendations**

---

# 🏗️ Future System Architecture

**Data Collection  
↓  
Data Processing  
↓  
Exploratory Analytics  
↓  
Statistical Validation  
↓  
Predictive Modeling  
↓  
Risk Assessment  
↓  
Recommendation Engine  
↓  
Interactive Dashboard**

---

# 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| SciPy | Statistical testing |
| Statsmodels | Statistical analysis and multiple-comparison correction |
| Jupyter Notebook | Interactive analysis environment |

---

# 📁 Project Structure

Seasonal-Agriculture-Performance-Analysis/

├── data/  
│   └── seasonal_agriculture_performance_dataset.csv  
│  
├── notebooks/  
│   └── seasonal_agriculture_analysis.ipynb  
│  
├── src/  
│  
├── outputs/  
│   ├── figures/  
│   └── tables/  
│  
├── docs/  
│  
├── .gitignore  
├── README.md  
└── requirements.txt

---

# ▶️ How to Run

## 1. Clone the Repository

Run the following command in your terminal:

    git clone https://github.com/TharunPranav2007/Seasonal-Agriculture-Performance-Analysis.git

## 2. Navigate to the Project Directory

    cd Seasonal-Agriculture-Performance-Analysis

## 3. Create a Virtual Environment

### Windows

    python -m venv .venv

Activate the environment:

    .venv\Scripts\activate

### macOS / Linux

    python3 -m venv .venv

Activate the environment:

    source .venv/bin/activate

## 4. Install Dependencies

    pip install -r requirements.txt

## 5. Launch Jupyter Notebook

    jupyter notebook

Open:

    notebooks/seasonal_agriculture_analysis.ipynb

Run the notebook sequentially from the beginning to reproduce the analysis.

---

# 🔁 Reproducibility

The project includes a `requirements.txt` file containing the dependencies required to reproduce the analysis.

For best results:

1. Create a virtual environment.
2. Install dependencies using `requirements.txt`.
3. Open the Jupyter Notebook.
4. Restart the kernel.
5. Run all cells from beginning to end.

The notebook contains the complete workflow from data preparation through analysis, statistical validation, insights, recommendations, limitations, and conclusion.

---

# 📚 Project Workflow

**Dataset  
↓  
Data Understanding  
↓  
Data Cleaning  
↓  
Feature Engineering  
↓  
Exploratory Data Analysis  
↓  
Seasonal Analysis  
↓  
Crop Analysis  
↓  
Irrigation & Resource Analysis  
↓  
Environmental Relationship Analysis  
↓  
Economic Analysis  
↓  
Risk Analysis  
↓  
Statistical Validation  
↓  
Key Findings  
↓  
Recommendations  
↓  
Limitations & Future Scope  
↓  
Conclusion**

---

# 🎯 Final Takeaway

The central insight from this project is that **seasonal agricultural performance is multi-dimensional**.

Agricultural decisions should not be evaluated using yield alone.

Environmental conditions, crop response, irrigation, resource efficiency, profitability, and disease/pest risk should be considered together.

The analysis provides a data-driven foundation for understanding seasonal agricultural performance and supports the development of future agricultural decision-support systems.

---

# 📌 Project Status

**Status:** Completed — Exploratory, Statistical, and Analytical Study

### Current Scope

- Data Preparation
- Exploratory Data Analysis
- Seasonal Analysis
- Crop Analysis
- Irrigation Analysis
- Resource Efficiency Analysis
- Environmental Relationship Analysis
- Economic Analysis
- Risk Analysis
- Statistical Validation
- Key Findings
- Data-Driven Recommendations
- Limitations
- Future Scope
- Conclusion

### Future Direction

- Predictive Analytics
- Real-Time Weather Integration
- Remote Sensing
- Risk Forecasting
- Interactive Dashboards
- Intelligent Agricultural Recommendation Systems

---

# 👨‍💻 Author

## Tharun Pranav T

**Project:** Seasonal Agriculture Performance Analysis

This project was developed as a comprehensive data analytics study focused on understanding seasonal agricultural performance using environmental, agricultural, resource, economic, and risk-related indicators.

---

# ⭐ Project Highlights

- 4,000 farm-level observations
- 28 analytical variables
- 3 agricultural seasons
- 8 crops
- 8 states
- 10 districts
- 4 irrigation methods
- Comprehensive exploratory data analysis
- Seasonal performance comparison
- Crop-level analysis
- Irrigation and water-efficiency analysis
- Economic and profitability analysis
- Disease/pest risk analysis
- Spearman correlation analysis
- Kruskal-Wallis testing
- Mann-Whitney U pairwise testing
- Bonferroni correction
- Chi-Square analysis
- Effect-size analysis
- Data-driven recommendations
- Future predictive analytics roadmap

---

## 🌱 Final Perspective

**Seasonal Agriculture Performance Analysis** demonstrates how agricultural data can be transformed into meaningful insights by combining environmental conditions, crop performance, resource utilization, economic outcomes, and risk indicators.

The project establishes a foundation for moving from descriptive agricultural analytics toward future predictive and intelligent decision-support systems.

**Author: Tharun Pranav T**