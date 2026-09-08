import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv("Smartphone_Sales.csv")

# Create Pair Plot
sns.pairplot(
    df,
    vars=["Price", "Rating", "Sales", "Discount", "Stock"],
    hue="Category",
    diag_kind="hist"
)

# Display the plot
plt.show()
<img width="1913" height="981" alt="Screenshot 2026-08-04 201805" src="https://github.com/user-attachments/assets/5bd5074c-7860-4cde-9814-ba078a4b1a19" />
