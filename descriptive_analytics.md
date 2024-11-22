# EX.No:2 Descriptive Analytics

## Aim:
To calculate summary statistics, analyze data distributions, measure relationships between variables, and visualize correlations using Python.
## Tools Required:
Python (NumPy, Pandas, Matplotlib, Seaborn)
## Procedure
## Part A: Summary Statistics and Data Distribution Analysis
```
1.Calculate Measures of Central Tendency
   Compute mean, median, and mode for the dataset.
2.Calculate Measures of Dispersion
   Calculate standard deviation, variance, and range.
3.Analyze Data Distribution
   Compute skewness and kurtosis to understand asymmetry and tail behavior.
```
## code:
```
import numpy as np
import pandas as pd
from scipy.stats import mode, skew, kurtosis

# Example data
data = [12, 15, 14, 10, 10, 8, 12, 14, 15, 10, 18, 20, 25, 30, 15, 14]

# Convert data to a Pandas Series for convenience
data_series = pd.Series(data)

# Calculate measures of central tendency
mean_value = data_series.mean()
median_value = data_series.median()
mode_value = mode(data_series)[0][0]

# Calculate measures of dispersion
std_dev = data_series.std()
variance = data_series.var()
data_range = data_series.max() - data_series.min()

# Analyze distribution
data_skewness = skew(data_series)
data_kurtosis = kurtosis(data_series)

# Display results
print("Summary Statistics:")
print(f"Mean: {mean_value}")
print(f"Median: {median_value}")
print(f"Mode: {mode_value}")
print(f"Standard Deviation: {std_dev}")
print(f"Variance: {variance}")
print(f"Range: {data_range}")
print(f"Skewness: {data_skewness}")
print(f"Kurtosis: {data_kurtosis}")
```
## Output:
![image](https://github.com/user-attachments/assets/7987901e-b22b-44ef-be92-a9988c4e1c95)
## 4.Explanation

## Central Tendency:
```
Mean: Average of the dataset values.
Median: Middle value when sorted.
Mode: Most frequently occurring value.
```
## Dispersion:
```
Standard Deviation: Measures the spread of data.
Variance: Square of the standard deviation.
Range: Difference between maximum and minimum values.
```
## Distribution Analysis:
```
Skewness: Positive skewness indicates a right tail.
Kurtosis: Describes tail behavior compared to normal distribution.
```
## Part B: Correlation and Covariance Analysis

## 1.Calculate Covariance and Correlation
```
Compute covariance to assess how variables vary together.
Calculate correlation to standardize relationships between variables.
```
## 2.Visualize Correlation Using Heatmaps
```
Generate a heatmap to represent relationships visually.
```
## code:
```
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Example dataset
data = {
    "Variable1": [10, 20, 30, 40, 50],
    "Variable2": [15, 25, 35, 45, 55],
    "Variable3": [12, 24, 36, 48, 60],
    "Variable4": [5, 10, 15, 20, 25],
}

# Convert to DataFrame
df = pd.DataFrame(data)

# Calculate Covariance
cov_matrix = df.cov()

# Calculate Correlation
corr_matrix = df.corr()

# Display Covariance and Correlation matrices
print("Covariance Matrix:")
print(cov_matrix)

print("\nCorrelation Matrix:")
print(corr_matrix)

# Visualize correlation using heatmap
plt.figure(figsize=(8, 6))
sns.heatmap(corr_matrix, annot=True, cmap="coolwarm", fmt=".2f")
plt.title("Correlation Heatmap")
plt.show()
```
## Output:

## Covariance Matrix:
```
Shows the extent to which variables change together.
```
![image](https://github.com/user-attachments/assets/d1b7fb8d-a40d-4a38-bc92-1d6ea167ca8c)

## Correlation Matrix:
```
Displays standardized relationships between variables ranging from -1 to +1.
```
![image](https://github.com/user-attachments/assets/f1a02f2c-fea6-42ad-8c48-9da278bdc9d1)

## Heatmap Visualization:
```
Graphical representation of correlation values.
```
![image](https://github.com/user-attachments/assets/0af44eea-cf1f-46bb-8074-3281f72c6499)

## Explanation
```
Covariance: Positive values imply variables increase together, and negative values imply the opposite.
Correlation: Standardizes covariance, with values closer to ±1 indicating strong relationships.
Heatmap: Visualizes relationships to identify patterns quickly.
```
## Result:
Descriptive analytics techniques were successfully applied to explore datasets, measure relationships, and visualize correlations effectively.








