Program 4: Box Plot – Confirmed Cases

# Program 4: Box Plot
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv("country_wise_latest.csv")

# Remove extra spaces
df.columns = df.columns.str.strip()

# Create Box Plot
plt.figure(figsize=(6,5))
plt.boxplot(df["Confirmed"])

plt.title("Box Plot of Confirmed Cases")
plt.ylabel("Confirmed Cases")
plt.grid(True)

plt.show()
<img width="893" height="458" alt="qw4" src="https://github.com/user-attachments/assets/6322e390-be34-4663-b1b6-97a6e7418110" />
