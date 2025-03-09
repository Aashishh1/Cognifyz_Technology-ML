<div align='center'><img style="width:30%" src='https://github.com/user-attachments/assets/83104b38-2fb7-4fb9-b46d-1ebcc21a5eac'/></div>

# Cuisine Classification🥗

## 📝 Project Overview
This project is a testament to my skills and passion for machine learning. The objective was to classify restaurants based on their cuisines by analyzing features such as restaurant names, cuisines, and the average cost for two. This project provided a hands-on opportunity to explore classification algorithms and understand their real-world applications.

---

## 📂 Dataset Information
**Dataset Description:**
- The dataset includes the following key features:
  - **Restaurant Name**: Identifies the establishment.
  - **Cuisines**: Lists the cuisine types served.
  - **Average Cost for Two**: Provides the cost details for two people.

**Preprocessing Steps:**
1. Dropped irrelevant columns (e.g., location, metadata fields).
2. Cleaned the data by removing rows with null values.
3. Encoded categorical variables using Label Encoding for model compatibility.
4. Standardized numerical features with `StandardScaler` for uniformity.

---

## 🛠️ Implementation Steps

| Step                | Description                                                                                 |
|---------------------|---------------------------------------------------------------------------------------------|
| **Data Preprocessing** | - Feature Selection: Retained only essential columns.<br>- Data Cleaning: Managed missing values efficiently.<br>- Encoding: Applied Label Encoding to convert categorical data into numerical form.<br>- Standardization: Used `StandardScaler` to normalize numerical features for better model performance. |
| **Model Training**    | Trained and evaluated two classification algorithms:<br>1. **Decision Tree Classifier**<br>&nbsp;&nbsp;&nbsp;&nbsp;- Criterion: Gini Index<br>&nbsp;&nbsp;&nbsp;&nbsp;- Accuracy: **24.36%**<br>2. **Logistic Regression**<br>&nbsp;&nbsp;&nbsp;&nbsp;- Configuration: Multinomial (for multi-class)<br>&nbsp;&nbsp;&nbsp;&nbsp;- Accuracy: **10.58%** |
| **Model Evaluation**  | Performance metrics used:<br>- Confusion Matrix<br>- Classification Report (Precision, Recall, F1-Score)<br>- Accuracy Score |

---

## 📊 Results Summary
| Model                | Accuracy  |
|----------------------|-----------|
| Decision Tree        | 24.36%    |
| Logistic Regression  | 10.58%    |

---

## 📚 Libraries Used
- **Numpy**: For numerical computations.
- **Pandas**: For data manipulation and analysis.
- **Scikit-learn**: For machine learning algorithms and evaluation.
- **Imbalanced-learn**: To handle data imbalance issues.
- **Matplotlib**: For data visualization.
- **Seaborn**: For advanced plotting and aesthetics.

---

_Thank you for checking out the project! 🌟_
