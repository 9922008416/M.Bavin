# M.Bavin
Data manipulation with pandas? 1.This task involves using the Pandas  library to manipulate data.  1. Loading a CSV file into a Pandas DataFrame  import pandas as pd
Data manipulation with pandas?
1.This task involves using the Pandas
 library to manipulate data.
 1. Loading a CSV file into a Pandas DataFrame
 import pandas as pd

# Load CSV file into a DataFrame
df = pd.read_csv('your_file.csv')

# Display the first few rows of the DataFrame
print(df.head())
 2. Filtering data based on conditions
 # Example: Filtering data based on a condition
filtered_data = df[df['column_name'] > 50]

# You can apply more complex conditions using logical operators (& for AND, | for OR)
filtered_data = df[(df['column1'] > 50) & (df['column2'] == 'value')]
 3. Handling missing values
 # Check for missing values
print(df.isnull().sum())

# Drop rows with any missing values
df.dropna(inplace=True)

# Fill missing values with a specific value
df.fillna(value=0, inplace=True)
 4. Calculating summary statistics
 # Summary statistics
summary_stats = df.describe()

# Calculate mean, median, etc. for specific columns
mean_value = df['column'].mean()
median_value = df['column'].median()
Example
 # Example workflow combining these operations
import pandas as pd

# Load data
df = pd.read_csv('your_file.csv')

# Display first few rows
print("First few rows of the DataFrame:")
print(df.head())

# Filter data
filtered_data = df[df['column_name'] > 50]
print("\nFiltered data where column_name > 50:")
print(filtered_data.head())

# Handle missing values
print("\nNumber of missing values in each column:")
print(df.isnull().sum())

df.dropna(inplace=True) # Drop rows with any missing values
print("\nDataFrame after dropping rows with missing values:")
print(df.head())

# Calculate summary statistics
summary_stats = df.describe()
print("\nSummary statistics:")
print(summary_stats)

mean_value = df['column'].mean()
print("\nMean of 'column':", mean_value)
