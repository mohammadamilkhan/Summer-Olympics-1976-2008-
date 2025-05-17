#  Olympic Data Analysis & Medal Prediction

This project explores historical Olympic data to uncover insights on athlete participation, medal trends, and sports dominance. It also implements machine learning models to predict medal outcomes based on various features.

---

### Problem Statement

The Olympic Games have long served as a global stage for athletic excellence, but the vast historical data on athletes, sports, and medal counts often remains underutilized. This project aims to analyze Olympic records from 1976 to 2008 to uncover participation trends, identify dominant countries and sports, and build predictive models to forecast medal outcomes using machine learning techniques.

---

### Objective

- Analyze Olympic data to identify trends in athlete participation and gender distribution.
- Explore country and sport-wise dominance in medal counts.
- Visualize key patterns using interactive and static plots.
- Build and evaluate classification models (Logistic Regression, Random Forest) to predict the type of medal an athlete may win.

## Dataset Overview

The dataset contains Olympic athlete and medal records from **1976 to 2008** with the following columns:

| Column Name  | Description                                        |
| ------------ | -------------------------------------------------- |
| City         | Host city of the Olympics                          |
| Year         | Year of the event                                  |
| Sport        | Main sport category (e.g., Aquatics, Athletics)    |
| Discipline   | Specific discipline under the sport                |
| Event        | Specific event (e.g., 100m sprint, 3m springboard) |
| Athlete      | Athlete's name                                     |
| Gender       | Gender of the athlete                              |
| Country_Code | Abbreviation of the athlete's country              |
| Country      | Full country name                                  |
| Event_gender | Gender category of the event                       |
| Medal        | Medal won (Gold, Silver, Bronze, or none)          |

---

## Key Insights

### 1.  Athlete Participation Trends

- Athlete participation steadily increased from 1976 to 2008.
- Significant rise in **female participation**, reducing the gender gap over time.

### 2. Top Medal-Winning Countries

- **United States** led with nearly 2,000 medals.
- Other strong performers: Soviet Union, Australia, Germany, China.

### 3. Most Medal-Rich Sports

- **Aquatics**, **Athletics**, and **Rowing** topped medal counts.
- Aquatics had over 2,200 medals due to a wide range of events.

---

## Machine Learning: Medal Prediction

### Logistic Regression

- **Accuracy:** ~34%
- Struggled with class imbalance and feature simplicity.
- Low precision and recall, especially for Silver medals.

### Random Forest (with GridSearchCV)

- **Accuracy:** ~53%
- Best Parameters: `max_depth=20`, `n_estimators=200`, `bootstrap=False`
- Achieved balanced performance across all medal classes.

---

## Conclusion

- The Olympics reflect rising **global and gender-inclusive participation**.
- **USA and Aquatics** dominate medals historically.
- **Random Forest** performs better than Logistic Regression for medal prediction, but improvements are needed with richer features.

---

## Recommendations

### Feature Engineering

- Add attributes like **age**, **previous medals**, or **event difficulty**.
- Replace `LabelEncoder` with **One-Hot Encoding** for nominal data.

### Class Balancing

- Use **SMOTE** or class weighting to address medal imbalance.

### Model Enhancement

- Try **XGBoost**, **LightGBM**, or deep learning models.
- Implement **cross-validation** for more reliable metrics.

### EDA Expansion

- Explore continent-wise trends and **event-level** dominance.

---

## Tech Stack

- Python, Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn (Logistic Regression, Random Forest, GridSearchCV)
- Jupyter Notebook for analysis and visualization

---
