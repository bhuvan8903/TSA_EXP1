# Ex.No: 01
# A PLOT A TIME SERIES DATA
###  Date:08/03/2025

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
```
import pandas as pd
import matplotlib.pyplot as plt

file_path = 'Time-Series Analysis Dataset.csv'  # Replace with your file path
data = pd.read_csv(file_path)

data['datetime_local'] = pd.to_datetime(data['datetime_local'])
data.set_index('datetime_local', inplace=True)

plt.figure(figsize=(10, 6))
plt.plot(data.index, data['temperature'], label='precip_intensity', color='blue')
plt.title('precipitation intensity today')
plt.xlabel('temperature')
plt.ylabel('precip_intensity')
plt.grid(True)
plt.legend()
plt.show()

plt.figure(figsize=(10, 6))

plt.hist(data['temperature'], bins=30, color='skyblue', edgecolor="black")

plt.title('preciptation')

plt.xlabel('temperature')

plt.ylabel('precip_intensity')

plt.show()

selected_columns = ['humidity', 'dew_point', 'wind_bearing', 'wind_speed','wind_gust','pressure','uv_index','ozone','precip_intensity','icon']

data[selected_columns].plot(kind='line', figsize=(15, 8))

plt.title('Line Plot for Selected Columns')

plt.xlabel('Datetime')

plt.ylabel('Precip_intensity')

plt.legend(loc='upper left')

plt.show()
```

# OUTPUT:
![image](https://github.com/user-attachments/assets/480dad4e-665a-4adf-a1f4-2595b618435c)

![image](https://github.com/user-attachments/assets/dbade84f-7d54-4da4-8710-98126e7a673b)

![image](https://github.com/user-attachments/assets/c61cefb3-c63d-4eba-a232-db7ecdcc80c4)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
