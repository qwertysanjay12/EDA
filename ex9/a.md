import pandas as pd
from scipy.stats import ttest_ind

# Load the dataset
df = pd.read_csv("Laptop_TTest_Dataset.csv")

# Create two groups
student = df[df["Category"] == "Student"]["Sales"]
gaming = df[df["Category"] == "Gaming"]["Sales"]

# Perform Independent Sample t-test
t_value, p_value = ttest_ind(student, gaming)

# Display results
print("t-value :", t_value)
print("p-value :", p_value)
<img width="205" height="26" alt="Screenshot 2026-09-01 181345" src="https://github.com/user-attachments/assets/e4a3e4ac-1433-4894-968c-89f9f8852aa1" />
