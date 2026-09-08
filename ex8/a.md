import pandas as pd

# Load dataset
df = pd.read_csv("Laptop_Rolling_Dataset.csv")

# Convert Date column into datetime format
df["Date"] = pd.to_datetime(df["Date"], dayfirst=True)

# Set Date as index
df.set_index("Date", inplace=True)

# Calculate Rolling Mean
df["Rolling_Mean"] = df["Sales"].rolling(window=7).mean()

# Calculate Rolling Standard Deviation
df["Rolling_SD"] = df["Sales"].rolling(window=7).std()

# Display result
print(df[["Sales", "Rolling_Mean", "Rolling_SD"]])
<img width="266" height="302" alt="Screenshot 2026-08-26 105002" src="https://github.com/user-attachments/assets/0471bcc5-a9ff-4028-b2ca-6c1c344e244c" />
