# Lesson 2 — Pandas

## Learning objectives

- Understand what pandas is.
- Create a DataFrame.
- Work with rows and columns.
- Explore a dataset.
- Add new columns.
- Calculate basic statistics.

## 1. What is pandas?

Pandas is a Python library used to organize, manage, and analyze data in tables.

First, import pandas:

```python
import pandas as pd
```

- `import` loads a library.
- `pandas` is the library name.
- `pd` is the short name used to access pandas functions.

## 2. Creating a dataset

A dataset is a collection of related information.

```python
import pandas as pd

data = {
    "Student": ["A", "B", "C", "D"],
    "Marks": [65, 75, 90, 58]
}

df = pd.DataFrame(data)

print(df)

```

Output:

| Student | Marks |
|---|---:|
| A | 65 |
| B | 75 |
| C | 90 |
| D | 58 |

A **DataFrame** is a table with rows and columns, similar to a spreadsheet.

- `pd.DataFrame(data)` converts the dictionary into a table.
- `df` stores the table.
- `print(df)` displays the table.

## 3. Working with columns

A column contains information such as student names or marks.

Display only student names:

```python
print(df["Student"])
```

Display only marks:

```python
print(df["Marks"])
```

Display both columns:

```python
print(df[["Student", "Marks"]])
```

Remember:

- `df["Marks"]` selects one column.
- `df[["Student", "Marks"]]` selects multiple columns.

## 4. Working with rows

Rows represent individual records in a dataset.

Select the first row:

```python
print(df.iloc[0])
```

Select the third row:

```python
print(df.iloc[2])
```

Select the first two rows:

```python
print(df.iloc[0:2])
```

Python uses zero-based indexing. The first row has index `0`, the second has index `1`, and the third has index `2`.

The ending index in `iloc[0:2]` is not included.

## 5. Exploring a dataset

| Code | Purpose |
|---|---|
| `df.head()` | Displays the first five rows by default |
| `df.tail()` | Displays the last five rows by default |
| `df.shape` | Shows the number of rows and columns |
| `df.columns` | Shows the column names |
| `df.info()` | Shows information about columns and data types |
| `df.describe()` | Summarizes numerical columns |

Example:

```python
print(df.shape)
```

Output:

```text
(4, 2)
```

This means the dataset has four rows and two columns.

## 6. Adding a new column

We can add a column to show each student's result.

```python
df["Result"] = ["Pass", "Pass", "Pass", "Fail"]

print(df)
```

Output:

| Student | Marks | Result |
|---|---:|---|
| A | 65 | Pass |
| B | 75 | Pass |
| C | 90 | Pass |
| D | 58 | Fail |

We can also create the result column using a condition:

```python
df["Result"] = df["Marks"].apply(
    lambda mark: "Pass" if mark >= 60 else "Fail"
)
```

This assigns "Pass" when marks are at least 60 and "Fail" otherwise.

## 7. Calculating the average

```python
print("Average marks:", df["Marks"].mean())
```

Output:

```text
Average marks: 72.0
```

The `mean()` function calculates the average of the marks column.

## 8. Complete practice program

```python
import pandas as pd

data = {
    "Student": ["A", "B", "C", "D"],
    "Marks": [65, 75, 90, 58]
}

df = pd.DataFrame(data)

print("Complete dataset:")
print(df)

print("\nStudent names:")
print(df["Student"])

print("\nFirst two students:")
print(df.iloc[0:2])

print("\nDataset size:")
print(df.shape)

print("\nAverage marks:")
print(df["Marks"].mean())
```

