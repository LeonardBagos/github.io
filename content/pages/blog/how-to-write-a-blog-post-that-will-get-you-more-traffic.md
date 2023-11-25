---
type: PostLayout
slug: project5
date: '2023-11-20'
excerpt: >-
  Sit ratione eligendi et quis distinctio et maiores accusantium aut accusamus
  facere sit repellat quidem qui alias nostrum et earum enim. Cum quis sint eos
  dolor quas ad odit ipsum qui quia eius.
featuredImage:
  url: /images/ff.png
  altText: Thumbnail
  type: ImageBlock
  styles:
    self:
      borderRadius: medium
content: |+


bottomSections: []
isFeatured: true
isDraft: false
seo:
  metaTitle: How to Write a Blog Post That Will Get You More Traffic
  metaDescription: You can add the excerpt and main keywords of your blog post here.
  socialImage: /images/abstract-feature2.svg
  type: Seo
colors: bg-light-fg-dark
styles:
  self:
    flexDirection: col
    textAlign: center
title: "Analyzing the Impacts of Daily Commuting in NCR, Philippines\_ \_ \_ \_ using Python Machine Learning"
---
**Abstract:** *Predicting the impacts of daily commuting and gauging commuter satisfaction though Data Science, encompassing statistical analysis with Excel, feature engineering via SQL, and machine learning implemented with Python*

![](https://miro.medium.com/v2/resize:fit:630/1*ogQJFT50-AFOAl6UOjBkHw.jpeg)

> **INTRODUCTION**

The National Capital Region (NCR) in the Philippines is grappling with the consequences of rapid urbanization and dense population, particularly evident in the daily commuting experiences of millions of residents. This intricate web of commuting, involving diverse transportation modes, has evolved into a complex phenomenon, significantly impacting the lives of NCR inhabitants.

![](https://miro.medium.com/v2/resize:fit:630/1*-UGPVvJTGZR2RGUCuiAr0g.png)

As the NCR continues to grow, understanding the far-reaching impacts of daily commuting on aspects such as traffic, environment, and economy is crucial for crafting effective solutions to benefit the region’s residents.

> **OBJECTIVES**

Facing the growing problems of traffic congestion, extended travel durations, mental adjustments, and health considerations, the focus of this analysis centers around three main goals.

![](https://miro.medium.com/v2/resize:fit:481/1*IrzrZXdrgg0FrK2r2rFIdw.png)

> **METHODOLOGY AND ANALYSIS**

This analysis is structured to comprehend the impacts of daily commuting in the National Capital Region (NCR) of the Philippines. It follows various steps to examine the experiences, challenges, and effects of daily commuting in this region.

![](https://miro.medium.com/v2/resize:fit:630/1*jCKHHZPbxqotdkMOviKVpQ.png)

The analysis utilizes the Data Analysis Tool pack in Microsoft Excel, which incorporates various statistical techniques.

![](https://miro.medium.com/v2/resize:fit:509/1*ZAwHEl56uQqB3BwHxWu4Ew.png)

To enhance the analysis, technical improvements are made to the raw data using PostgreSQL. In PostgreSQL, the focus is on feature engineering, preparing the data for machine learning in Python.

![](https://miro.medium.com/v2/resize:fit:400/1*KlI0G5o-3M1m3adBiyAOuQ.png)

> **RESULTS AND DISCUSSIONS**

In this section, we unveil the insights garnered from our analysis, offering a condensed overview of key findings.

![](https://miro.medium.com/v2/resize:fit:630/1*IxcKxo42nJi3Vqx-zb---g.png)

The findings highlight a significant dissatisfaction rate, with a striking 80% of the 40 respondents expressing discontent with the current transport system.

![](https://miro.medium.com/v2/resize:fit:570/1*hUUKdLCbTcCZPa_iepGDIA.png)

Additionally, the study identifies four key impacts of commuting: Unbalanced Life and Time, Less Productivity and Tardiness, Exhaustion or Low Energy, and Health Risks. Notably, ‘Unbalanced Life and Time’ emerges as the most prominent concern, while only a small portion, 3%, express concerns about health risks.

![](https://miro.medium.com/v2/resize:fit:561/1*PK6Xba7ey-uKqgIfGyReTw.png)

Among the notable findings, ‘Unbalanced Life and Time’ emerges as strongly correlated to exhaustion or low energy, overall satisfaction, and the rating score of commuters.

![](https://miro.medium.com/v2/resize:fit:630/1*Z2GvEAwhtCeVIQo3W-MruA.png)

The findings reveal that factors such as gender, transport modes, number of trips, and distance traveled have minimal impact on overall satisfaction levels. However, a crucial revelation emerges as the time spent commuting significantly influences satisfaction.

*We will not focus on the results of our statistical analysis here. But you can check the detailed discussion here. (*[*result\&findings.pdf*](https://drive.google.com/file/d/1BEuqSDbKvQw2gI7ONG3dhMlA6QT3tGIk/view?usp=sharing)*)*

> **Feature Engineering in SQL**

In the feature engineering phase conducted in SQL, we implemented various techniques to enhance the data’s suitability for machine learning in Python. Here is a summary of the key feature engineering steps:

![](https://miro.medium.com/v2/resize:fit:630/1*0wTaQlqZT-T2hUopHCaRaA.png)

As a result of these feature engineering techniques, the dataset was enriched with 19 features, providing a diverse set of inputs for machine learning models.

Now, we will discuss the most important part of the study.

# **Machine Learning using Python**

In this section, we undertake a binary classification task to predict the satisfaction level of commuters. This involves the following steps:

1.  Perform an exploratory analysis (scaling, PCA, unbalanced)

2.  Split the data (train, validation, test)

3.  Perform 10-fold cross-validation and grid search.

4.  Compare the different classification methods (Logistic Regression, K-Nearest Neighbors, Support Vector Machines, Random Forest, XGBoost)

5.  Show evaluation metrics (ROC-AUC, accuracy, F1 score)

First, import the required packages and the dataset.

```
##First, Import the required packages
import pandas as pd
import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt

##For Scaling and Transformation
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA

##For Training 
from sklearn.model_selection import train_test_split, cross_val_score, GridSearchCV, StratifiedKFold
from tqdm import tqdm

##For Classification
from sklearn.linear_model import LogisticRegression
from sklearn.svm import SVC
from sklearn.ensemble import RandomForestClassifier
from xgboost import XGBClassifier
from sklearn.neighbors import KNeighborsClassifier

##For Evaluation
from sklearn.metrics import roc_auc_score, accuracy_score, f1_score
from sklearn.metrics import confusion_matrix
```

```
##Import the dataset

df = pd.read_csv('commutesurvey.csv')
df.columns
def als_split_data(df):
    output = df['satisfied']
    features = pd.DataFrame(data=df)
    cols = ['id', 'satisfied']
    for col in cols:
        if col in features.columns:
            features = features.drop(col, axis=1)
    return output, features
output, features = als_split_data(df)
df.head()
```

The above is an example of what the dataset looks like. Below is a statistical description of the 19 dataset features.

![](https://miro.medium.com/v2/resize:fit:630/1*bYWM_VZUJ0JskhaeCFVQbQ.png)

```
display(features.describe())
```

![](https://miro.medium.com/v2/resize:fit:630/1*u7GB8l8JFioOfrK344t48Q.png)

Visualize the distribution statistics; apply appropriate data preprocessing steps.

```
fig, axes = plt.subplots(4, 5, figsize=(10, 10))

axes = axes.flatten()


for i, col in enumerate(features):
    sns.histplot(df[col], kde=True, ax=axes[i])
    axes[i].set_title(col)


for j in range(i+1, 10):
    fig.delaxes(axes[j])

plt.tight_layout()
plt.show()
```

![](https://miro.medium.com/v2/resize:fit:444/1*pNYQ5mAB591OHePuH3zaHg.png)

Visualizing feature correlations.

```
plt.figure(figsize=(12, 10))
sns.heatmap(features.corr(), cmap='RdYlGn', annot=True, fmt='.2f') 
plt.show()
```

![](https://miro.medium.com/v2/resize:fit:453/1*ofmOJbSXk1AKCqYl8c0V_Q.png)

Below is the distribution of Satisfied column after preprocessing.

```
colors = ['red', 'green']

plt.figure(figsize=(6, 4))
df['satisfied'].value_counts().plot(kind='bar', color=colors, edgecolor='black')
plt.title('Distribution of Satisfaction')
plt.xlabel('Satisfaction')
plt.ylabel('Frequency')
plt.show()
```

![](https://miro.medium.com/v2/resize:fit:383/1*cfMtZKSpRDN2bfi8UI0gHQ.png)

Feature transformation by PCA.

```
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA

X = df.drop('satisfied', axis=1)
y = df['satisfied']

# Scale the features
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Apply PCA
pca = PCA(n_components=16)
X_pca = pca.fit_transform(X_scaled)

plt.figure(figsize=(10, 6))
plt.plot(range(1, len(pca.explained_variance_ratio_)+1), pca.explained_variance_ratio_.cumsum())
plt.title('Cumulative Explained Variance')
plt.xlabel('Number of Principal Components')
plt.ylabel('Cumulative Explained Variance')
plt.show()
```

![](https://miro.medium.com/v2/resize:fit:517/1*CYq_JIzpBUK6SdTPu1BRUQ.png)

The above graph indicates that 100% of variance in the data can be achieved with just 16 dimensions instead of the 19 features.

```
plt.figure(figsize=(10, 6))
plt.scatter(X_pca[:, 0], X_pca[:, 1], c=y, cmap='viridis')
plt.xlabel('First Principal Component')
plt.ylabel('Second Principal Component')
plt.title('PCA - First Two Principal Components')
plt.show()
```

![](https://miro.medium.com/v2/resize:fit:518/1*46-MrIqsnu72ZbmV_Tgmyw.png)

As can be seen from the above plots, quite a good classification is achieved with just 2 dimensions.

**Train, Validate and Test**

```
from sklearn.model_selection import train_test_split, cross_val_score, GridSearchCV


# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X_pca, y, test_size=0.2, random_state=42)

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

Showing the train and test scores:

```
models = {
    'Logistic Regression': LogisticRegression(solver='liblinear'),
    'KNN': KNeighborsClassifier(n_neighbors=7),
    'SVM': SVC(),
    'Random Forest': RandomForestClassifier(n_estimators=1, random_state=0),
    'XGBoost': XGBClassifier(gamma=0, learning_rate=0.1, n_estimators=10, n_jobs=1, nthread=None, objective='binary:logistic', random_state=0)
}

results = {'Model': [], 'Train Score': [], 'Test Score': []}

##Some of the codes were removed for copyright purposes and intellectual property

plt.xlabel('Models')
plt.ylabel('Scores')
plt.title('Train and Test Scores of Different Models')
plt.xticks([i + bar_width / 2 for i in index], models)
plt.legend()
plt.tight_layout()

plt.show()
```

![](https://miro.medium.com/v2/resize:fit:597/1*Fg9Lij_REwdsHw_ZY9-9eQ.png)

Among the classifiers, **Random Forest** exhibited the highest training score, reaching 0.9, showcasing its proficiency in capturing patterns within the training data. However, when assessed on the test set, Logistic Regression and XGBoost emerged as the top performers, both achieving an accuracy of 0.85.

**Cross Validation and Grid Search**

```
models = [
    {'name': 'Logistic Regression', 'model': LogisticRegression(solver='liblinear'), 'params': {'C': [0.1, 1, 10]}},
    {'name': 'Support Vector Machines', 'model': SVC(), 'params': {'C': [0.1, 1, 10], 'gamma': [0.1, 1, 10]}},
    {'name': 'Random Forest', 'model': RandomForestClassifier(), 'params': {'n_estimators': [100, 200, 300], 'max_depth': [None, 5, 10]}},
    {'name': 'XGBoost', 'model': XGBClassifier(use_label_encoder=False, eval_metric='logloss'), 'params': {'n_estimators': [100, 200, 300], 'max_depth': [3, 5, 7]}},
    {'name': 'KNN', 'model': KNeighborsClassifier(), 'params': {'n_neighbors': [3, 5, 7]}}  # KNN added to models
]

# Perform 10-fold cross-validation and grid search for all models
## Some codes were removed here
    m['best_score'] = grid.best_score_
    m['best_params'] = grid.best_params_

for m in models:
    print(f"Model: {m['name']}\nBest Score = {m['best_score']}\nBest Params = {m['best_params']}\n{'=' * 30}")
```

![](https://miro.medium.com/v2/resize:fit:405/1*CWn_enie0jZVfkmFEZxdvg.png)

Now, we can compare and evaluate the metrics for each models.

**Comparison and Evaluation**

```
# Define the parameters for each model
logreg_params = {'solver':'liblinear','C': 10} 
knn_params = {'n_neighbors': 7}   
svc_params = {'C': 10, 'gamma': 0.1}  
forest_params = {'n_estimators': 300, 'max_depth': 10}  
xg_reg_params = {'max_depth': 3, 'n_estimators': 200} 

# Initialize the models with defined parameters
logreg = LogisticRegression(**logreg_params)
knn = KNeighborsClassifier(**knn_params)
svc = SVC(**svc_params)
forest = RandomForestClassifier(**forest_params)
xg_reg = XGBClassifier(**xg_reg_params)
 

model_test_data_dict = {
    'Logistic Regression': (logreg, X_test, y_test),
    'KNN': (knn, X_knntest, y_knntest),
    'SVM': (svc, X_test, y_test),
    'Random Forest': (forest, X_test, y_test),
    'XGBoost': (xg_reg, X_test, y_test)
}
```

```
metrics = ['ROC-AUC', 'Accuracy', 'F1-Score']
values = {model_name: {metric: [] for metric in metrics} for model_name in model_test_data_dict}

for model_name, (model, X_test, y_test) in model_test_data_dict.items():
    y_pred = model.predict(X_test)
    values[model_name]['ROC-AUC'] = roc_auc_score(y_test, y_pred)
    values[model_name]['Accuracy'] = accuracy_score(y_test, y_pred)
    values[model_name]['F1-Score'] = f1_score(y_test, y_pred)

fig, ax = plt.subplots(figsize=(10, 6))

bar_width = 0.1
index = range(len(metrics))

for i, (model_name, scores) in enumerate(values.items()):
    bars = plt.bar([x + i * bar_width for x in index], list(scores.values()), bar_width, label=model_name)
    for bar in bars:
        plt.text(bar.get_x() + bar.get_width() / 2, bar.get_height(), f'{bar.get_height():.2f}', ha='center', va='bottom')

plt.xlabel('Metrics')
plt.ylabel('Scores')
plt.title('Evaluation Metrics for Different Models')
plt.xticks([i + bar_width for i in index], metrics)

plt.legend(loc='center left', bbox_to_anchor=(1, 0.5))
plt.tight_layout()
plt.show()
```

![](https://miro.medium.com/v2/resize:fit:600/1*4jSIaI6Kcsp7oFjTZngU-Q.png)

The model evaluation results suggest that XGBoost is the most promising model for this classification task, displaying superior performance across multiple metrics. The best model is XGBoost, as it has the highest ROC-AUC (0.83), indicating better ability to distinguish between classes. XGBoost has the highest F1-Score (0.67), which is important if you want a balance between precision and recall. We also compare them through confusion matrices.

```
metrics = ['ROC-AUC', 'Accuracy', 'F1-Score']
confusion_matrices = {model_name: None for model_name in model_test_data_dict}

for model_name, (model, X_test, y_test) in model_test_data_dict.items():
    y_pred = model.predict(X_test)
    
    # Compute confusion matrix
    cm = confusion_matrix(y_test, y_pred)
    confusion_matrices[model_name] = cm

    # Compute other metrics
    roc_auc = roc_auc_score(y_test, y_pred)
    accuracy = accuracy_score(y_test, y_pred)
    f1 = f1_score(y_test, y_pred)
    
    values[model_name]['ROC-AUC'] = roc_auc
    values[model_name]['Accuracy'] = accuracy
    values[model_name]['F1-Score'] = f1

# Plotting the confusion matrices
fig, axes = plt.subplots(nrows=2, ncols=3, figsize=(10, 10))

for i, (model_name, cm) in enumerate(confusion_matrices.items()):
    ax = axes[i // 3, i % 3]
    sns.heatmap(cm, annot=True, fmt='d', cmap='Blues', cbar=False, ax=ax)
    ax.set_title(f'Confusion Matrix - {model_name}')
    ax.set_xlabel('Predicted')
    ax.set_ylabel('True')

plt.tight_layout()
plt.show()
```

![](https://miro.medium.com/v2/resize:fit:440/1*oem6_twyqIMM8QbOLBymxQ.png)

> **CONCLUSIONS**

The analysis on how daily commuting affects people in the National Capital Region (NCR) of the Philippines took a deep dive into various analyses. What follows is a summary of what we discovered, highlighting the many problems and possible ways to make daily commuting in the region.

![](https://miro.medium.com/v2/resize:fit:630/1*NgB98hoYmRJb4c-MTeisMQ.png)

> **RECOMMENDATIONS**

The following recommendations aim to bridge the gap between the findings of our study and real-world improvements in the daily lives of NCR commuters.

![](https://miro.medium.com/v2/resize:fit:630/1*pNdL7aPaibXbK31mEon3Sg.png)

These recommendations aim to bridge the gap between research insights and practical applications, fostering a proactive approach towards enhancing the daily commuting experience in the National Capital Region.

> **REFERENCES:**

Fallaria, A. J., de Jesus, R., Carpio, M., Jacinto, F. L., De Leon, L., Agapito, J., & Ramos, J. G. (2019). Emerging from the ‘worst’: An ethnography of the modern Filipino commuting culture behind the Metro Manila traffic crisis. In MATEC Web of Conferences (Vol. 272, p. 01032). EDP Sciences.

Mijares, A. C., Suzuki, M., & Yai, T. (2013). Equity Analysis of Urban Rail Fare Policy and Passenger Overload Delay: An International Comparison and the Case of Metro Manila MRT-3. Journal of the Eastern Asia Society for Transportation Studies, 10, 45–66.

Polintan, B. (2022, October 24). Impacts of Worsening Traffic on Daily Commuters. Crown Asia Lifestyle Blog. Retrieved from <https://www.crownasia.com.ph/lifestyle-blog/impacts-of-worsening-traffic-to-daily-commuters/>

