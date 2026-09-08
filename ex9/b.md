import pandas as pd
from scipy.stats import ttest_ind

# Load the dataset
df = pd.read_csv("Laptop_TTest_Dataset.csv")

# Create two groups
student = df[df["Category"] == "Student"]["Sales"]
gaming = df[df["Category"] == "Gaming"]["Sales"]

# Perform Independent Sample t-test
t_value, p_value = ttest_ind(student, gaming)

# Significance level
alpha = 0.05

print("t-value :", t_value)
print("p-value :", p_value)

# Conclusion
if p_value < alpha:
    print("\nConclusion:")
    print("Reject the Null Hypothesis (H0)")
    print("There is a significant difference between the Sales of Student and Gaming laptops.")
else:
    print("\nConclusion:")
    print("Fail to Reject the Null Hypothesis (H0)")
    print("There is no significant difference between the Sales of Student and Gaming laptops.")
    <img width="518" height="79" alt="Screenshot 2026-09-01 181449" src="https://github.com/user-attachments/assets/508a11c4-acd8-4a0d-b9c4-16af1531e07c" />
