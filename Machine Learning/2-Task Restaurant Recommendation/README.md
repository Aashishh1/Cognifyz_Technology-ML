<div align='center'><img style="width:30%" src='https://github.com/user-attachments/assets/8d7109de-962a-47a0-b7ba-50663778dd0b'/></div>


# Restaurant Recommendation🍽️

🚀 **Restaurant Recommendation System** is a robust application that helps users find the best dining options based on their preferences. Using a content-based filtering approach, it recommends restaurants tailored to the user's tastes.

## ✨ Features
- 📜 **Data Preprocessing**: Efficiently handles missing values, removes duplicates, and encodes categorical data for analysis.
- 🍽️ **Cuisine Preference Filtering**: Matches restaurants based on cuisine similarity.
- 💰 **Price and Rating Based Recommendations**: Prioritizes restaurants within a specific price range and high aggregate ratings.
- 🔍 **Content-Based Filtering**: Utilizes Jaccard similarity to recommend restaurants similar to the user's preferences.
- 📈 **High-Quality Output**: Focuses on restaurants with ratings of 4.0 and above for reliable recommendations.
---

## 🧠 Workflow
### 1. Load Dataset
The system reads and displays the input dataset for exploration and analysis.
### 2. Preprocess Data
- Handles missing values.
- Drops duplicate records for cleaner data.
- Encodes categorical variables such as cuisines for compatibility with the model.
### 3. Filter Criteria
- Retains restaurants with an aggregate rating of 4.0 and above.
### 4. Similarity Calculation
- Calculates Jaccard similarity scores between restaurants based on cuisines.
### 5. Recommend Restaurants
- Displays the top 5 recommended restaurants sorted by similarity and aggregate ratings.

## 🛠️ Implementation
### 1. Preprocessing the Dataset
Efficiently cleans and organizes the dataset for analysis.
```python
dfRS = df[['Restaurant ID', 'Restaurant Name', 'Cuisines', 'Aggregate rating', 'Votes']]
dfRS = dfRS.dropna()
dfRS = dfRS.sort_values(by=['Restaurant Name', 'Aggregate rating'], ascending=False).drop_duplicates('Restaurant Name', keep='first')
```
### 2. Similarity Calculation
Generates a cross-tabulation of cuisines and computes Jaccard similarity scores.
```python
jaccardDist = pdist(xTabRestoCuisines.values, metric='jaccard')
jaccardSim = 1 - squareform(jaccardDist)
dfJaccard = pd.DataFrame(jaccardSim, index=xTabRestoCuisines.index, columns=xTabRestoCuisines.index)
```
### 3. Recommendations
Fetches the top 5 similar restaurants based on user input.
```python
input_restaurant = 'Ooma'
sim = dfJaccard.loc[input_restaurant].sort_values(ascending=False)
sim = sim[(sim.index != input_restaurant) & (sim >= 0.7)].head(5)
recommendations = pd.merge(sim.reset_index(), dfRS[['Restaurant Name', 'Aggregate rating']], left_on='index', right_on='Restaurant Name').sort_values('Aggregate rating', ascending=False)
```

## 📝 Output
For the input restaurant `Ooma`, the system recommends:
| Restaurant Name | Similarity Score | Aggregate Rating |
|-----------------|------------------|------------------|
| Nobu           | 1.0              | 4.4              |
| Nagai          | 1.0              | 4.3              |
| Ichiban        | 1.0              | 4.3              |
| Osaka          | 1.0              | 4.2              |
| Guppy          | 1.0              | 4.1              |

## 📊 Data Insights
- **Total Restaurants Analyzed:** 1236
- **Unique Cuisines Identified:** 753
- **Filtered Restaurants (Rating >= 4.0):** 954

🌟 **Happy Dining! 🍽️**
---
_Thank you for checking out the project! 🌟_
