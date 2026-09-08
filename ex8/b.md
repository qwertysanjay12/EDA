import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv("Laptop_Rolling_Dataset.csv")

# Convert Date column
df["Date"] = pd.to_datetime(df["Date"], dayfirst=True)

# Set index
df.set_index("Date", inplace=True)

# Rolling Mean
df["Rolling_Mean"] = df["Sales"].rolling(window=7).mean()

# Plot
plt.figure(figsize=(10,5))

plt.plot(df.index, df["Sales"], label="Original Sales")
plt.plot(df.index, df["Rolling_Mean"], linewidth=3, label="7-Day Rolling Mean")

plt.title("Laptop Sales vs 7-Day Rolling Mean")
plt.xlabel("Date")
plt.ylabel("Sales")
plt.legend()
plt.show()
<img width="907" height="468" alt="Screenshot 2026-08-26 105102" src="https://github.com/user-attachments/assets/c46b7c1d-f947-466e-9160-51cf075ea401" />
