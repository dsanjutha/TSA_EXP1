# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 25.10.2026

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```python
from matplotlib import pyplot as plt
import pandas as pd

df = pd.read_csv("cars_dataset.csv")
print(df.head())
df['year'] = pd.to_datetime(df['year'], format='%Y')
print(df.dtypes)
df.set_index('year',inplace=True)
df_resampled=df['price'].resample('YS').mean()
df_resampled.plot(kind='line',label='Total Sales',color='black')
plt.title('Time Series Plot of Car Prices Each Year')
plt.xlabel('Year')
plt.ylabel('Average Car Price')
plt.legend()
plt.grid(True)
```



















# OUTPUT:
<img width="971" height="543" alt="ex1(a) output" src="https://github.com/user-attachments/assets/96d24910-9319-461e-a5a3-9f6de27fac9d" />













<img width="908" height="596" alt="ex1(a) output(graph)" src="https://github.com/user-attachments/assets/1014902a-a8bd-4177-b53f-5876909329df" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
