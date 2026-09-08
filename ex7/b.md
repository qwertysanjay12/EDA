import pandas as pd

# Load the dataset
df = pd.read_csv("Laptop_Sales.csv")

# Convert Date column into datetime format
df["Date"] = pd.to_datetime(df["Date"], dayfirst=True)

# Set Date column as index
df.set_index("Date", inplace=True)

# Down-Sampling (Daily to Monthly)
monthly_data = df.resample("ME").mean(numeric_only=True)

# Up-Sampling (Monthly to Daily)
daily_data = monthly_data.resample("D").ffill()

# Display the result
print("Up-Sampled Daily Data")
print(daily_data.head(15))
<img width="532" height="90" alt="Screenshot 2026-08-18 230304" src="https://github.com/user-attachments/assets/14c49ae7-1721-4dee-8089-653885645f4a" />
