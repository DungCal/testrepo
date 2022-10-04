import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

df_iris = pd.read_csv("https://raw.githubusercontent.com/phamdinhkhanh/datasets/master/iris_train.csv", header=0, index_col=None)

df_iris.head()

df_iris.describe()

#Tiếp theo chúng ta sẽ xem độ dài cánh hoa trung bình ở mỗi loài là bao nhiêu:

df_summary=df_iris[['Species', 'Petal.Length']].groupby('Species').mean()

x, y = list(df_summary.index), df_summary['Petal.Length'].values
