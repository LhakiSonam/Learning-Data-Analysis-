
# Lesson 1: Understanding and Analyzing Data

## 1. What Is a Dataset?

A dataset is a collection of related information. For example, suppose we collect the mathematics test marks of five students.

| Student | Mathematics Marks |
|:---:|---:|
| A | 65 |
| B | 80 |
| C | 72 |
| D | 90 |
| E | 58 |

We can analyze this dataset to answer questions such as:

- What is the average mark?
- What is the highest mark?
- What is the lowest mark?
- How many students scored above 70?

Python can help us answer all these questions.

## 2. Store the Data in Python

We can use a Python list to store the marks.

```python
marks = [65, 80, 72, 90, 58]

print(marks)
```


**Output:**

```text
[65, 80, 72, 90, 58]
```

Here, `marks` is a variable containing a list of five numbers. Each number represents one student's test result.

## 3. Calculate Useful Statistics

Python has built-in functions that help us analyze numerical data.

```python
marks = [65, 80, 72, 90, 58]

print("Total:", sum(marks))
print("Number of students:", len(marks))
print("Average:", sum(marks) / len(marks))
print("Highest:", max(marks))
print("Lowest:", min(marks))
```
<img width="1470" height="956" alt="Screenshot 2026-10-22 at 3 06 00 PM" src="https://github.com/user-attachments/assets/cddfe206-7cfb-47da-8598-ac40aab1e4d5" />

**Output:**

```text
Total: 365
Number of students: 5
Average: 73.0
Highest: 90
Lowest: 58
```
<img width="1450" height="912" alt="Screenshot 2026-10-22 at 3 06 39 PM" src="https://github.com/user-attachments/assets/28b673e0-15e7-4ee9-a808-3684d4d51ca9" />


### Understanding the Functions

| Function | Purpose |
|---|---|
| `sum(marks)` | Calculates the total of all marks. |
| `len(marks)` | Counts the number of marks. |
| `sum(marks) / len(marks)` | Calculates the average mark. |
| `max(marks)` | Finds the highest mark. |
| `min(marks)` | Finds the lowest mark. |

## 4. Find Students Who Scored Above 70

We can use a loop and a condition to identify marks greater than 70.

```python
marks = [65, 80, 72, 90, 58]

for mark in marks:
    if mark > 70:
        print(mark)
```

**Output:**

```text
80
72
90
```

This helps us identify which marks are above 70.

## 5. What I Learned

- A dataset is a collection of related information.
- Python lists can store numerical data.
- Built-in functions can calculate useful statistics.
- Loops and conditions can help us find specific values in a dataset.



*End of Lesson 1*
