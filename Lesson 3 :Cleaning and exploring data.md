# Lesson 3 — Cleaning and Exploring Data

## 1. What Is Data Cleaning?

Data cleaning is the process of identifying and correcting problems in a dataset.

Common problems include:
- Missing values
- Duplicate records
- Incorrect data
- Inconsistent information

For example, a student may have no mark recorded, or the same student may appear twice in a dataset.

## 2. Creating a Dataset

First, import pandas and create a sample dataset.

```python
import pandas as pd

data = {
    "Student": ["A", "B", "C", "D", "D"],
    "Marks": [65, 75, None, 58, 58]
}

df = pd.DataFrame(data)

print(df)
```

In this dataset:
- Student C has a missing mark.
- Student D appears twice.
- `None` represents a missing value.

## 3. Identifying Missing Values

Use `isnull()` to identify missing values.

```python
print(df.isnull())
```

To count missing values in each column:

```python
print(df.isnull().sum())
```

The output shows that the `Marks` column contains one missing value.
<img width="1470" height="956" alt="Screenshot 2026-10-23 at 3 58 18 pm" src="https://github.com/user-attachments/assets/daafdb02-bda5-44d2-ba76-4e2aff97256a" />

What the code does
- df.isnull().sum() counts missing values in each column.
- df.isnull().any(axis=1) identifies rows containing at least one missing value.
- df[...] displays those rows.

## 4. Removing Duplicate Records

Duplicate records are repeated entries in a dataset.

Use `duplicated()` to identify duplicates.

```python
print(df.duplicated())
```

Use `drop_duplicates()` to remove repeated rows.

```python
df = df.drop_duplicates()
print(df)
```
<img width="1318" height="233" alt="Screenshot 2026-10-23 at 4 00 36 pm" src="https://github.com/user-attachments/assets/51b7361c-37e5-4e3c-9550-b24d988ecf8f" />

OUTPUT
<img width="627" height="392" alt="Screenshot 2026-10-23 at 4 04 50 pm" src="https://github.com/user-attachments/assets/e1870a11-def4-4c76-85f8-73abda3a7f64" />


What does this code do?
- df.duplicated() identifies rows that are repeated.
- df[df.duplicated()] displays the duplicate rows.
- df.drop_duplicates() removes duplicate rows, keeping the first occurrence.
- print(df) displays the cleaned dataset.

This keeps the first occurrence of each identical row.

## 5. Exploring a Dataset

Data exploration helps us understand the structure and characteristics of our data.

Here are some useful pandas commands:

| Code | Purpose |
|---|---|
| `df.head()` | Displays the first five rows |
| `df.tail()` | Displays the last five rows |
| `df.shape` | Shows the number of rows and columns |
| `df.columns` | Displays column names |
| `df.info()` | Shows column information and data types |
| `df.describe()` | Summarizes numerical data |
| `df.isnull().sum()` | Counts missing values |

Example:

```python
print("Dataset size:", df.shape)
print("\nColumn names:")
print(df.columns)

print("\nDataset information:")
df.info()

print("\nSummary statistics:")
print(df.describe())
```

These commands help us understand the dataset before performing further analysis.

## 6. Filtering Data

Filtering allows us to select rows that meet a particular condition.

For example, suppose we want to find students who scored at least 70 marks.

```python
data = {
    "Student": ["A", "B", "C", "D"],
    "Marks": [65, 75, 90, 58]
}

df = pd.DataFrame(data)

high_marks = df[df["Marks"] >= 70]

print(high_marks)
```

Output:

| Student | Marks |
|---|---:|
| B | 75 |
| C | 90 |

The condition `df["Marks"] >= 70` selects students whose marks are 70 or higher.

## 7. Sorting Data

Sorting arranges records in ascending or descending order.

### Lowest to highest

```python
print(df.sort_values("Marks"))
```

### Highest to lowest

```python
print(df.sort_values("Marks", ascending=False))
```

The `ascending=False` argument sorts the marks from highest to lowest.

## 8. Summarizing Data

Pandas can calculate statistics that help us understand our dataset.

```python
print("Average marks:", df["Marks"].mean())
print("Highest marks:", df["Marks"].max())
print("Lowest marks:", df["Marks"].min())
print("Total students:", df["Student"].count())
```

These calculations summarize the marks and help us identify patterns in the data.

## 9. Complete Practice Program

```python
import pandas as pd

data = {
    "Student": ["A", "B", "C", "D", "D"],
    "Marks": [65, 75, None, 58, 58]
}

df = pd.DataFrame(data)

print("Original dataset:")
print(df)

print("\nMissing values:")
print(df.isnull().sum())

print("\nDuplicate records:")
print(df.duplicated())

# Remove duplicate records
df = df.drop_duplicates()

# Remove rows with missing values
df = df.dropna()

print("\nCleaned dataset:")
print(df)

print("\nDataset summary:")
print(df.describe())

print("\nStudents with marks of 60 or higher:")
print(df[df["Marks"] >= 60])

print("\nStudents sorted by marks:")
print(df.sort_values("Marks", ascending=False))
```

## 10. What I Learned

In this lesson, I learned how to identify missing values, detect and remove duplicate records, explore a dataset, filter rows, sort information, and calculate summary statistics using pandas.

## 11. Practice Questions

1. What is data cleaning?
2. What does `df.isnull().sum()` do?
3. What is the difference between `dropna()` and `drop_duplicates()`?
4. How can you select students who scored more than 80 marks?
5. Which pandas command sorts marks from highest to lowest?

