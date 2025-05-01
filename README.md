# 🎧 Predicting Podcast Listening Time - Kaggle Playground Series S5E4

A regression project built for the [Kaggle Playground Series - Season 5, Episode 4](https://www.kaggle.com/competitions/playground-series-s5e4), where the goal was to predict how long users would listen to a given podcast episode based on various metadata features.

## 📌 Problem Statement

Given structured metadata such as episode title, genre, host/guest popularity, and sentiment, the task is to **predict the number of minutes a user will listen to a podcast episode**. The competition is evaluated using **Root Mean Squared Error (RMSE)**.

---

## 🧠 Features in the Dataset

- Podcast_Name  
- Episode_Title  
- Episode_Length_minutes  
- Genre
- Host_Popularity_percentage
- Publication_Day 
- Publication_Time  
- Guest_Popularity_percentage  
- Number_of_Ads 
- Episode_Sentiment  
- Listening_Time_minutes (target)

---

## ⚙️ Approach & Pipeline

### 🔨 Feature Engineering
- Extracted episode number from `Episode_Title`
- Mapped and encoded:
  - Categorical labels (Podcast Name, Genre, Time of Day, etc.)
  - Sentiment and publication time into numerical/categorical codes
- Created high-order interaction features by combining:
  - Episode length, ad count, sentiment, publication day/time, and episode number using 2-way to 4-way combinations

### 🧪 Model Training
- Model: **LightGBM Regressor**
- 5-Fold Cross Validation with:
  - Early stopping
  - Averaged predictions from all folds
- Evaluation metric: **RMSE**
- Final public leaderboard RMSE: **12.850**

---

## 🧪 Libraries Used

- pandas, numpy, seaborn, matplotlib
- `lightgbm
- category_encoders
- scikit-learn
- tqdm

---

## 🚀 How to Run the Code

1. Clone the repo or open in Kaggle
2. Make sure your dataset path matches:
3. Run the notebook or script
4. The final predictions will be saved to "submission.csv"

---

## 📈 Evaluation

- **RMSE**: ~12.85068

---

## 🙌 Acknowledgements

Thanks to Kaggle and the organizers of the Playground Series S5E4.  
Inspired by other excellent community notebooks on feature engineering and ensemble modeling.

---

