Program 5: Scatter Plot – Confirmed vs Deaths

# Program 5: Scatter Plot
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Remove extra spaces
df.columns = df.columns.str.strip()

# Create Scatter Plot
plt.figure(figsize=(8,5))
plt.scatter(df["Confirmed"], df["Deaths"])

plt.title("Confirmed vs Deaths")
plt.xlabel("Confirmed Cases")
plt.ylabel("Deaths")
plt.grid(True)

plt.show()
<img width="872" height="461" alt="qw5" src="https://github.com/user-attachments/assets/91948e89-74dd-41dc-a466-f5e0db5b429c" />
