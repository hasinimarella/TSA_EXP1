# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 12-08-2025

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
import matplotlib.pyplot as plt\
df=pd.read_csv('/content/blood_donor_dataset.csv')
df.shape
df1=df.head()
df
df.info()
df.describe()
df = df.sort_values('months_since_first_donation')

plt.plot(df['months_since_first_donation'], df['pints_donated'], marker='o')
plt.xlabel("Months Since First Donation")
plt.ylabel("Pints Donated")
plt.title("Pints Donated Over Time Since First Donation")
plt.grid(True)
plt.show()
df['created_at'] = pd.to_datetime(df['created_at'])
df = df.sort_values('created_at')

plt.plot(df['created_at'], df['pints_donated'])
plt.xlabel("Date")
plt.ylabel("Blood Donations")
plt.title("Blood Donations Over Time")
plt.grid(True)
plt.show()
```
# OUTPUT:
<img width="1703" height="691" alt="image" src="https://github.com/user-attachments/assets/a7a8e7ce-d833-4e1f-b30f-960536ebd7ee" />
<img width="621" height="392" alt="Screenshot 2025-08-19 081425" src="https://github.com/user-attachments/assets/38c02044-56bb-47c2-96d2-356b2c0559a6" />
<img width="605" height="355" alt="Screenshot 2025-08-19 081434" src="https://github.com/user-attachments/assets/3dd8cf23-5b87-4211-a7c8-03779ba4fef9" />
<img width="795" height="636" alt="Screenshot 2025-08-19 081442" src="https://github.com/user-attachments/assets/b3e92886-7d85-49cd-9a4b-a9c2c6c6d29d" />
<img width="657" height="662" alt="Screenshot 2025-08-19 081451" src="https://github.com/user-attachments/assets/75d13a5c-829d-4713-82fe-6a7e5a57e8c2" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
