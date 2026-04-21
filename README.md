# Ex.No: 01A PLOT A TIME SERIES DATA

###  Date:20/04/26

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

```py
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("/content/drive/MyDrive/COLAB PROJECTS/Time Series/House_Price.csv")
df['year'] = df['YearBuilt']

yearly_data = df.groupby('year')['Price'].mean()

yearly_data.plot(kind='line', marker='o')
plt.title('Average House Price per Year')
plt.xlabel('Year')
plt.ylabel('Average Price')
plt.grid(True)
plt.show()
```

# OUTPUT:

<img width="777" height="593" alt="image" src="https://github.com/user-attachments/assets/5cc9b711-53e2-4a2e-91cd-8d7094bca133" />




# RESULT:
Thus we have created the python code for plotting the time series of given data.
