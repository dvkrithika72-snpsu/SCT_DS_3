# Bank Marketing Subscription Predictor

## 🔍 Project Overview
This project focuses on building a **Predictive Machine Learning Model** using a Decision Tree Classifier to analyze data from a Portuguese banking institution's direct marketing campaigns. The primary business goal is to predict whether a targeted customer will subscribe to a term deposit (indicated by the target variable `y` as a "Yes" or "No").

By automating this process, the bank can optimize its marketing strategies, save operational costs, and target only the customers who have a high probability of converting.

---

## 🛠️ Methodology & Technical Architecture
The workflow was implemented in a clean, sequential pipeline using **Python** and standard data science libraries within a Jupyter Notebook environment:

1. **Data Preprocessing & Cleaning:** Separated the independent features (client demographics, account details, and campaign history) from the target variable (`y`) out of the semi-colon-separated dataset (`bank.csv`).
2. **Feature Engineering (One-Hot Encoding):** Converted text-based categorical columns (such as `job`, `marital` status, `education`, and `housing` loans) into binary numeric formats using `pd.get_dummies()`.
3. **Data Splitting:** Stratified the dataset into a **70% Training set** and a **30% Testing set** using `train_test_split` to ensure balanced class distributions.
4. **Model Training:** Trained a `DecisionTreeClassifier` utilizing **Entropy** to measure information gain, enforcing a strict **Maximum Depth of 5 levels** (`max_depth=5`) to prevent overfitting.

---

## 📊 Key Insights & Visual Deliverables
* **The Confusion Matrix Heatmap:** Provides a clear breakdown of True Positives, True Negatives, False Positives, and False Negatives, reflecting high overall classification performance.
* **The Decision Tree Flowchart Layout:** Maps out the exact logical conditions the algorithm uses to evaluate a customer. 

> 💡 **Primary Business Conclusion:** The root node of the generated tree reveals that **`duration` (call duration)** is the most crucial determining factor in a campaign's success. If a telemarketing phone conversation with a client crosses a specific threshold (approximately 3.5 minutes), the conversion probability climbs dramatically. Secondary features like **`poutcome_success`** also act as heavy indicators of customer interest.

---

## 💻 Technologies & Frameworks Used
* **Development Environment:** Visual Studio Code (VS Code) with Jupyter Notebooks (Python 3.11.9 Kernel).
* **Data Manipulation:** `pandas`
* **Machine Learning Engine:** `scikit-learn`
* **Data Visualization & Graphics:** `matplotlib` & `seaborn`
