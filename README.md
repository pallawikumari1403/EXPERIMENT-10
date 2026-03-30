# Experiment-10:
## Aim:To study the basics of the Pandas library in Python, including creation and manipulation of Series and DataFrames.

## Theory:
Pandas is a powerful Python library used for data analysis and manipulation. It provides two main data structures:
# Series: One-dimensional labeled array
# DataFrame: Two-dimensional labeled data structure (like a table)

## Code Explanation:

# 1. Creating a Series:
import pandas as pd
s = pd.Series([10,20,30,40])
print(s)
Creates a one-dimensional array with default indexing.
# 2. Creating a DataFrame:
data = {
    "Name":["A","B","C"],
    "Marks":[85,90,78]
}
df = pd.DataFrame(data)
print(df)
Creates a table with columns Name and Marks.
# 3. Basic Attributes of DataFrame:
print(df.shape)   # Rows and columns
print(df.ndim)    # Number of dimensions
print(df.size)    # Total elements
# 4. Column Information:
print(df.columns) # Column names
print(df.dtypes)  # Data types of columns
# 5. Accessing Data:
print(df["Name"])        # Access column
print(df.loc[0,"Name"])  # Access using label
print(df.iloc[2,1])      # Access using index
# 6. Adding a New Column:
df["Grade"] = ["First Class","Distinction","Second class"]
print(df)
# 7. Updating Data:
df.loc[0,"Marks"] = 88   # Using loc
df.iloc[0,1] = 88        # Using iloc
print(df)
# 8. Deleting a Column:
df.drop("Grade", axis=1, inplace=True, errors="ignore")
print(df)
# 9. Statistical Operations:
mean1 = df["Marks"].mean()
min1 = df["Marks"].min()
max1 = df["Marks"].max()
# 10. Conditional Filtering:
df[df["Marks"]>80]
Displays students with marks greater than 80.
## Output Summary:
Successfully created Series and DataFrame.
Performed operations like accessing, updating, adding, and deleting data.
Applied statistical functions and filtering.
## Conclusion:
This experiment demonstrates how to use Pandas for basic data handling and analysis. It helps in understanding how to efficiently manipulate structured data in Python.
