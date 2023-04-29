# Gold-Price-Prediction
The gold price prediction is an ML project using Randomforest model.
code:
import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor
df = pd.read_csv('/content/gold_price.csv')
print(df.shape)
df.head()
df.info()
df.isnull().sum()
plt.figure(figsize = (10,5))
sns.heatmap(corr, cbar=True)
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size = 0.2, random_state=2)
ml = RandomForestRegressor(n_estimators=100)
test_data_prediction = ml.predict(X_test)
print('Accuracy on training data: ',ml.score(X_test, Y_test))
