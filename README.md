# data-cleaning-using-ml-
import pandas as pd 
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt 
import kagglehub

# Download latest version
path = kagglehub.dataset_download("himelsarder/retail-product-dataset-with-missing-values")

print("Path to dataset files:", path)
import os

path = r"C:\Users\user\.cache\kagglehub\datasets\himelsarder\retail-product-dataset-with-missing-values\versions\1"

print(os.listdir(path))


dataset = pd.read_csv(r"C:\Users\user\.cache\kagglehub\datasets\himelsarder\retail-product-dataset-with-missing-values\versions\1\synthetic_dataset.csv")
dataset.head(5)
dataset.shape
(dataset.isnull().sum()/dataset.shape[0])*100
(dataset.isnull().sum().sum()/(dataset.shape[0]*dataset.shape[1]))*100
sns.heatmap(dataset.isnull())
plt.show()
#this is the intro part or code for data cleaning new 
