# 🦟 Dengue Cases Prediction – Machine Learning Project

Machine learning project based on the **DengAI: Predicting Disease Spread** competition from DrivenData.  
The objective is to predict the number of dengue fever cases in two cities using environmental and climate variables.

This project explores the complete machine learning workflow, including **exploratory data analysis (EDA), feature engineering, model comparison, and hyperparameter optimization** to build a predictive model capable of estimating weekly dengue cases.

---

## 📁 Repository Structure

The project is organized into modular directories to ensure scalability and order:

```
├── assets/                  # Images and visual content (e.g., for README banner)
├── calibration_process/     # Scripts and images for intrinsic camera calibration
├── complete_padel_system/   # Unified application integrating Security + Tracker
├── security_system/         # Independent biometric pattern recognition module
├── tracking_system/         # Independent ball tracking and umpire logic module
│
├── .gitignore               # Git configuration
├── README.md                # Project documentation
├── documentation.pdf        # Final report and project documentation
└── requirements.txt         # Dependencies and required libraries
```


# 📌 Project Overview

Dengue fever is a mosquito-borne disease influenced by environmental factors such as temperature, humidity, and vegetation.

In this project, machine learning models are trained to predict the **total number of dengue cases per week** based on historical environmental data.

The dataset includes observations from two cities:

- **San Juan, Puerto Rico**
- **Iquitos, Peru**

Each observation contains meteorological and satellite-derived variables that may influence mosquito population dynamics and disease transmission.

The goal is to build a model that can accurately estimate dengue case counts based on these predictors.

---

# 🎯 Objective

Develop a predictive machine learning model capable of estimating weekly dengue cases using environmental variables.

The project focuses on:

- Understanding the dataset through **exploratory data analysis**
- Identifying important predictors related to dengue transmission
- Comparing different machine learning models
- Improving model performance through **hyperparameter optimization**
- Evaluating models using the competition metric (**Mean Absolute Error – MAE**)

---

# 📊 Dataset

The dataset originates from the **DrivenData DengAI competition**.

It includes:

- Climate variables (temperature, humidity, precipitation)
- Vegetation indexes
- Atmospheric conditions
- Weekly dengue case counts

The data is split by city due to their **different climate patterns and epidemiological dynamics**.

Example features include:

- `reanalysis_air_temp_k`
- `reanalysis_specific_humidity_g_per_kg`
- `station_avg_temp_c`
- `ndvi_ne`
- `precipitation_amt_mm`

Target variable:
- **`total_cases`**
which represents the number of dengue cases reported in a given week.

---

# 🔍 Exploratory Data Analysis

Initial analysis was performed to understand:

- Feature distributions
- Correlations with dengue cases
- Missing values
- Differences between the two cities

Key steps included:

- Distribution analysis of meteorological variables
- Correlation heatmaps
- Time series visualization
- City-specific exploratory analysis

The analysis revealed that **humidity, temperature, and vegetation indices** show meaningful relationships with dengue case counts.

---

# ⚙️ Machine Learning Approach

Several machine learning models were tested to identify the best-performing approach.

Models explored include:

- Random Forest Regressor
- Gradient Boosting models
- XGBoost

The workflow followed these steps:

1. Data preprocessing  
2. Handling missing values  
3. Feature scaling when necessary  
4. Model training using cross-validation  
5. Hyperparameter optimization  

---

# 🚀 Hyperparameter Optimization

To improve model performance, several hyperparameter tuning techniques were applied.

### Randomized Search

`RandomizedSearchCV` was used to explore a wide range of hyperparameters efficiently.  
This approach samples random combinations from the search space, allowing a broad exploration with lower computational cost compared to exhaustive search.

### Grid Search

After identifying promising parameter ranges, `GridSearchCV` was applied to perform a more detailed search around the best candidates.  
This method evaluates all combinations of specified hyperparameters and helps refine model performance.

### Optuna

Finally, **Optuna** was used for more advanced hyperparameter optimization.  
Optuna uses Bayesian optimization techniques to efficiently search the hyperparameter space and automatically focus on the most promising configurations.

Optimization included parameters such as:

- number of estimators
- maximum tree depth
- learning rate
- subsampling ratios
- minimum samples per leaf

This multi-stage optimization strategy helped improve the final model performance.

---

# 📈 Model Evaluation

The competition evaluation metric is:

**Mean Absolute Error (MAE)**

Lower MAE values indicate better predictive performance.

The best-performing model achieved:

**MAE: 25.60**

This result was obtained using **XGBoost with optimized hyperparameters**, demonstrating strong predictive capability on the evaluation set.

---

# 🧠 Key Takeaways

This project demonstrates the complete machine learning workflow applied to a real-world prediction problem.

Main insights include:

- Environmental variables contain valuable signals for predicting dengue outbreaks
- Tree-based ensemble models perform well on tabular climate data
- Hyperparameter optimization significantly improves model performance
- Careful exploratory analysis helps identify meaningful predictors

---

# 🛠️ Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- Optuna  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

---


# 🔮 Possible Improvements

Future improvements could include:

- Time-series feature engineering (lags and rolling windows)
- City-specific models
- Ensemble models combining multiple algorithms
- Temporal cross-validation strategies

---

# 📚 References

DrivenData Competition:

DengAI – Predicting Disease Spread  
https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/

---

## 👤 Author

Javier Piay  
Industrial Engineer | Big Data & AI 

📫 Connect with me on [LinkedIn](https://www.linkedin.com/in/javier4piay)

