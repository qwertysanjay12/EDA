import pandas as pd
from scipy.stats import ttest_ind

# Load the dataset
df = pd.read_csv("Laptop_TTest_Dataset.csv")

# Separate the two groups
student = df[df["Category"] == "Student"]["Sales"]
gaming = df[df["Category"] == "Gaming"]["Sales"]

# Perform Independent Sample t-test
t_value, p_value = ttest_ind(student, gaming)

# Display results
print("t-value :", round(t_value, 4))
print("p-value :", round(p_value, 4))
<img width="151" height="23" alt="Screenshot 2026-09-01 183225" src="https://github.com/user-attachments/assets/e653c30b-ad3d-4a2e-92ad-78c768edf926" />
