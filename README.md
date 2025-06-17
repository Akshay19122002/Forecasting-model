# Forecasting-project

import pandas as pd 
import openpyxl
import matplotlib.pyplot as plt
from statsmodels.tsa.arima.model import ARIMA
from sklearn.linear_model import LinearRegression

# Load dummy data
df = pd.read_excel('dummy_sales_data.xlsx')
print(df.head())

# Clean and sort data
df['Date'] = pd.to_datetime(df['Date'])
df = df.sort_values('Date')

# Plot sales over time
plt.plot(df['Date'], df['Sales'])
plt.title("Sales Over Time")
plt.xlabel("Date")
plt.ylabel("Sales")
plt.show()


