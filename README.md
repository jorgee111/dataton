# 🥇 Madrid Traffic Accidents · I NeuralHack Datathon (Winner)

**Winning solution of the I NeuralHack Datathon (2025, Universidad Europea de Madrid): analysis of Madrid's traffic-accident records and a model that predicts how serious the injuries are.**

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jorgee111/dataton/blob/main/madrid_traffic_accidents_analysis.ipynb)

## 🎯 The challenge

Given ~86,000 accident records from the city of Madrid (date, time, district, weather, type of accident, vehicle, person, age range…), predict the **injury severity level** (*lesividad*, 3 classes) of each person involved.

## 🔍 What the notebook does

1. **Data cleaning:** removes records that leak between train and test, handles nulls, duplicates and unknown values, and transforms dates, times and coordinates.
2. **Exploratory analysis:** accidents by sex, severity, type of accident, weekday, hour, age range, type of person and vehicle, plus a **heat map of accident locations in Madrid** (Folium).
3. **Feature engineering:** encoding of categorical variables and date features; correlation analysis.
4. **Class balancing with SMOTE**, because the dataset is strongly skewed towards one severity level.
5. **Random Forest** model and predictions for the test set.

## 📊 Results

| Class | Precision | Recall | F1 |
|---|---|---|---|
| 1 | 0.94 | 0.97 | 0.95 |
| 2 | 0.93 | 0.82 | 0.87 |
| 3 | 0.88 | 0.94 | 0.91 |

**~91 % accuracy on the validation set** (36,910 records). On the hidden test set the score was about 10 points lower: validation was done after balancing with SMOTE, which makes it optimistic. The notebook's conclusions discuss this and how the model could be improved.

## 🛠️ Stack

Python · pandas · scikit-learn · imbalanced-learn (SMOTE) · Plotly · Folium · seaborn

> The interactive Folium map was removed from the saved outputs because of its size (130 MB); run the cell to regenerate it. Plotly charts are saved as static images.

## 👤 Author

**Jorge de la Peña Jiménez** · [LinkedIn](https://www.linkedin.com/in/jorge-de-la-peña-jiménez-ab8610299) · [GitHub](https://github.com/jorgee111)

MIT License
