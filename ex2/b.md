Program 2: Pie Chart – Top 5 Countries by Confirmed Cases

# Program 2: Pie Chart
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Select top 5 countries with highest confirmed cases
top5 = df.sort_values(by="Confirmed", ascending=False).head(5)

# Create Pie Chart
plt.figure(figsize=(7,7))
plt.pie(top5["Confirmed"], labels=top5["Country/Region"], autopct='%1.1f%%')
plt.title("Top 5 Countries by Confirmed Cases")
plt.show()<img width="486" height="438" alt="qw2" src="https://github.com/user-attachments/assets/5f0168e0-ecc8-4a1f-aa7b-55316fc1fa63" />
