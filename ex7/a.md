import pandas as pd

# Load the dataset
df = pd.read_csv("Laptop_Sales.csv")

# Convert Date column into datetime format (DD/MM/YYYY)
df["Date"] = pd.to_datetime(df["Date"], format="%d/%m/%Y")

# Set Date as index
df.set_index("Date", inplace=True)

# Down-Sampling (Daily to Monthly)
monthly_data = df.resample("ME").sum(numeric_only=True)

print("Monthly Summary")
print(monthly_data)
<img width="526" height="101" alt="Screenshot 2026-08-18 230223" src="https://github.com/user-attachments/assets/c93e1696-3f0a-4af7-be44-5acc47fafa9d" />
