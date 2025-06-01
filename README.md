# Risk-tech hackathon Ak Bars bank (Риск-Тех Хакатон Ак Барс Банк)
Kaggle competition link: https://www.kaggle.com/competitions/ak-bars-real-estate-assessment-competition/overview

Here is top-1 solution for the hackathon task
## Team: **Torchки**

Kirill Shumskii (Innopolis University, Data Science and Artificial Intelligence): https://github.com/I-y6o-I

Arthur Babkin (Innopolis University, Data Science and Artificial Intelligence): https://github.com/ArthurBabkin

Adel Chernyatov (KFU, Applied Mathematics and Informatics): https://github.com/AdelChernyatov

# Problem
In this competition, Ak Bars Bank proposes to develop an algorithm (estimation model) using a wide range of features
over a long period to predict prices for residential real estate in Kazan.
Participants will be provided with data sets, including data obtained from different real estate aggregators at different periods of time,
as well as a set of features from the site https://mingkh.ru.

# Solution
## EDA
Research of features/target distribution was done. 
For the most of missing values we ised mean/mode filling. 
This approach is not semantically correct, but due to low feature importance of filled features this approach worked. 
In terms of hackathon this filling solution was made due to lack of time. For proper filling further research is needed.
For "District" feature we parsed latitude and longitude of certain address, then used KNN for fillig "District feature"
## Model
We used Catboost model with Optuna hyperparameter tuning

# Results
Top-1 on open and closed tests

**RMSE:** 21473.243

# Other hypotheses
We tried different boosting models such as XGBoost, LGMB, but CatBoost showed best metrics.
Also we tried SMOTER generation, but didnt get any meaningful results due to lack of time.
Pseudo labelig attempt for "Year of building" also was done, but we did't achive needed metrics for pseudo-labeling


# Further work
For achiviend more precise results several approaches are proposed:
- Sythetic data augmentation (SMOTER)
- Other models achitectures (MLP, TABM)
- Fearure engeneering
- Other features pseudo-labeling

