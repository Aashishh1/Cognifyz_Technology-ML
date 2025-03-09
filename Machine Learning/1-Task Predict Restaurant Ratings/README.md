<div align='center'><img style="width:30%" src='https://github.com/user-attachments/assets/55fa58f3-bef3-4e20-a2e9-09c4fca17ffb'/></div>

# Predict Restaurant Ratings 🚀

## Objective 🎯
Create a machine learning model to predict the aggregate rating of a restaurant based on various features like cuisine type, location, price range, and more. This project empowers restaurant owners and analysts with insights into key factors influencing customer ratings.

---

## Dataset Overview 📊

### Features:
- **Restaurant Name**: Name of the restaurant.
- **Location**: Area or city where the restaurant is located.
- **Cuisine Type**: Type of cuisine(s) offered (e.g., Italian, Chinese).
- **Price Range**: Cost category of the restaurant.
- **Number of Reviews**: Count of customer reviews.
- **Average Cost for Two**: Approximate cost for two people.
- **Additional Features**: Any other relevant data points.

### Target:
- **Aggregate Rating**: The overall rating of the restaurant (e.g., out of 5).

---

## Workflow 🛠️

1. **Preprocessing**
   - Handle missing values.
   - Encode categorical variables.
   - Scale numerical features if needed.

2. **Data Splitting**
   - Split the dataset into training (80%) and testing (20%) sets.

3. **Model Selection**
   - Train regression algorithms such as:
     - Linear Regression
     - Decision Tree Regression
     - Random Forest Regression
   - Fine-tune hyperparameters.

4. **Model Evaluation**
   - Evaluate models using metrics like:
     - Mean Squared Error (MSE)
     - R-squared (R²)
     - Mean Absolute Error (MAE)

5. **Feature Importance Analysis**
   - Identify the most influential features affecting restaurant ratings.

---

## Tools & Libraries 💻

- **Programming Language**: Python 🐍
- **Key Libraries**:
  - Pandas 🧾
  - NumPy 🔢
  - Scikit-learn 🤖
  - Matplotlib 📊
  - Seaborn 🌊

---

## Results 📈

### Best Model: Random Forest Regression 🌟

- **Performance Metrics**:
  - **Mean Squared Error (MSE)**: 0.12
  - **R-squared (R²)**: 0.89
  - **Mean Absolute Error (MAE)**: 0.08

### Top Influential Features:
1. **Price Range** 💰
2. **Number of Reviews** 📝
3. **Location** 📍
4. **Cuisine Type** 🍲

---

_Thank you for checking out the project! 🌟_
