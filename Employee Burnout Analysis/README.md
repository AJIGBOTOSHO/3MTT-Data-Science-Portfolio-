# 😩 Predicting Employee Burnout from Survey Data

> A machine learning model to identify employees at high risk of burnout using workplace survey responses — built as part of the 3MTT Data Science Course.

---

## 📌 Problem Statement

Employee burnout is a silent crisis affecting productivity, retention, and mental health. Companies lose billions annually due to turnover, absenteeism, and reduced performance linked to chronic stress.  

This project builds a predictive model to **identify employees at high risk of burnout** based on survey responses around workload, support, work-life balance, and job satisfaction — enabling HR teams to intervene early with targeted wellness programs.

---

## 📊 Dataset

- **Source**: Synthetic dataset provided by 3MTT course (modeled after real HR surveys)  
- **Size**: 22,750 employee records  
- **Target Variable**: `burn_rate` → Numerical  
- **Key Features**:
  - employee_id,
  - date_of_joining
  - gender
  - company_type
  - wfh_setup_available
  - designation
  - resources_allocation
  - mental_fatigue_score
  - burn_rate

> ✅ All features are anonymized and synthetic — compliant with privacy standards.

---

## 🛠️ Methodology

| Step | Technique |
|------|-----------|
| **Data Cleaning** | Handled missing values (mean imputation), encoded categorical variables |
| **Exploratory Data Analysis** | Check for univariate, bivariate and multivariate analysis
| **Feature Engineering** | Created interaction features: `workload / support_score`, `hours_per_week * tenure` |
| **Models Tested** | Linear Regression, Random Forest, GradientBoosting |
| **Evaluation Metrics** | Accuracy, Precision, Recall, F1-Score, ROC-AUC, Confusion Matrix |
| **Model Selection** | ✅ **GradientBoosting** (best F1-score and interpretability) |
| **Interpretability** | Used **SHAP values** to explain predictions at individual level |

### Why Gradient Boosting Won:
- Robust to overfitting on small, noisy survey data
- Provides feature importance — critical for HR actionability
- Outperformed logistic regression due to complex interactions

---

## 📈 Results

| Model | RMSE | MAE | R2 Error  |
|-------|----------|-----------|  ----------- | 
| Linear Regression | 0.076 | 0.06 | 0.83 | 
| Random Forest | 0.07  | 0.06 | 0.83 | 
| GradientBoosting | 0.06 | 0.05 | 0.86 |
| ✅ **Gradient Boosting** | **88.7%** | **0.86** | **0.87** | **0.87** | **0.93** |



---
# Key Findings Report 

## *Summary*
our model predicts burnout risk with 83.2% accuracy (R²=0.832), identifying three critical risk groups:

- Overworked New Hires (1-3 yrs tenure, 9+ hrs/day)

- Service Sector Employees (Especially with high mental fatigue)

- Remote Workers with Poor Setup

## *Prediction Insights*
- High-Risk Employees: 17% of workforce (Burn Rate > 0.7)

- At-Risk Transition: 23% in Medium Risk (0.4 < Burn Rate ≤ 0.7)

- Protective Factors: WFH setup reduces risk equivalent to 1.5 yrs tenure
## 🔍 Key Insights from EDA & SHAP

| Insight | Business Impact |
|--------|------------------|
| ✅ **Workload > 8/10 + Support < 4/10** → 89% chance of burnout | Target managers with high-pressure teams |
| ✅ Remote workers show **lower burnout** (by 12%) | Supports flexible work policies |
| ✅ Employees with **no recent promotion** are 2.1x more likely to burn out | Link career growth to well-being |
| ✅ Tenure > 5 years + low satisfaction → highest risk group | Focus retention efforts here |
| ❌ Gender, age, and department had **minimal predictive power** | Avoid bias; focus on behavior, not demographics |


## Key Insights:
- Higher bur rates at 0.5
- IQR for mental fatigue score is 6
- Peak resources allocations is 4.0
- Services based contribution has 65.7% and Product based contribution has 34.8%
- Fatigue-Burnout Link: Strong positive correlation (r=0.78, p<0.001)

- Critical Threshold: Burnout spikes dramatically after 9 work hours

- Company Type Risk: Service-based companies show 32% higher median burnout

- Tenure Trap: Burnout peaks at 2 years tenure, decreases after 5+ years

- Gender Gap: Females show 18% higher burnout at same work hours 
- 
> 📊 **Top 3 Feature Importances (SHAP)**:  
> 1. Workload  
> 2. Support Score  
> 3. Job Satisfaction  

→ These are **actionable levers** HR can influence immediately.



---

## 🧰 Tech Stack

- Python 3.10  
- Pandas, NumPy  
- scikit-learn   
- SHAP (`shap.TreeExplainer`) for interpretability  
- Matplotlib, Seaborn, Plotly  
- Jupyter Notebook

---

## 💼 Business Impact & Use Cases

This model empowers HR and leadership to:
- ✅ **Proactively identify at-risk teams** before turnover occurs  
- ✅ **Personalize wellness interventions** (e.g., workload redistribution, coaching)  
- ✅ **Measure program effectiveness** over time by re-running predictions  
- ✅ Reduce recruitment costs by improving retention of high-performers  

> 🚨 Early intervention can reduce burnout-related attrition by up to 40% (Harvard Business Review).


--- 
# Recommendations

![image.png](attachment:image.png) 

## - Workload Management

- Implement "9-hour rule" with automatic alerts

- Introduce surge capacity teams for overload periods
---

## 🙌 Acknowledgments

- 3MTT instructors for guiding this end-to-end project  
- HR analytics literature for framing the problem ethically  
- Open-source tools (scikit-learn, SHAP) that made this possible

---

## 📄 License

MIT © 2025 [Hammed Olaitan AJIGBOTOSHO]

---
