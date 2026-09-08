import pandas as pd
from scipy.stats import ttest_ind

# Load the dataset
df = pd.read_csv("Laptop_TTest_Dataset.csv")

# Separate the two groups
student = df[df["Category"] == "Student"]["Sales"]
gaming = df[df["Category"] == "Gaming"]["Sales"]

# Perform Independent Sample t-test
t_value, p_value = ttest_ind(student, gaming)

# Significance level
alpha = 0.05

print("t-value :", round(t_value, 4))
print("p-value :", round(p_value, 4))

# Interpretation
if p_value < alpha:
    print("\nStatistical Conclusion:")
    print("The difference between Student and Gaming laptop sales is statistically significant.")
    print("\nLayman Interpretation:")
    print("The difference in sales is real and not due to chance.")
    print("The business can confidently make decisions based on this result.")
    print("For example, more investment can be made in the better-performing category.")

else:
    print("\nStatistical Conclusion:")
    print("The difference between Student and Gaming laptop sales is not statistically significant.")
    print("\nLayman Interpretation:")
    print("The observed difference may have occurred by chance.")
    print("There is not enough evidence to change business strategies based on this result.")
    <img width="518" height="113" alt="Screenshot 2026-09-01 183415" src="https://github.com/user-attachments/assets/2461632e-e9d0-46f1-9360-e5dc625baba6" />
