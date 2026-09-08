Program 3: Histogram – Confirmed Cases Distribution

# Program 3: Histogram
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Remove extra spaces from column names
df.columns = df.columns.str.strip()

# Create Histogram
plt.figure(figsize=(8,5))
plt.hist(df["Confirmed"], bins=10, edgecolor="black")
plt.title("Distribution of Confirmed Cases")
plt.xlabel("Confirmed Cases")
plt.ylabel("Frequency")
plt.grid(True)
plt.show()
<img width="890" height="470" alt="qw3" src="https://github.com/user-attachments/assets/3ca7905a-5123-41a6-8764-8beb6a11c840" />
