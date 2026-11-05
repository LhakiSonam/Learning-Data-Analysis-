# Lesson 4: Graphs and Visualization

## 1. What is Data Visualization?

Data visualization is the process of representing data using visual elements such as graphs, charts, and diagrams. It helps us understand information, identify patterns, and compare data more easily.

## 2. Why is Data Visualization Important?

- Makes data easier to understand.
- Helps identify patterns and trends.
- Makes comparing information easier.
- Presents complex information in a simple way.
- Helps communicate results clearly.

## 3. Python Libraries for Data Visualization

Python has different libraries that help us create graphs and charts.

**Pandas**
- Used to organize and analyze data.
- Helps create and manage datasets using DataFrames.

**Matplotlib**
- A Python library used to create graphs and charts.
- Allows us to visualize data in different ways.

To use these libraries, we import them:

```python
import pandas as pd
import matplotlib.pyplot as plt
```
<img width="1441" height="714" alt="Screenshot 2026-11-05 at 10 01 25 AM" src="https://github.com/user-attachments/assets/12ff5efe-9d8f-42b0-82ca-6cbdcd4a4572" />


## 4. Types of Graphs

### A. Bar Graph
A bar graph uses rectangular bars to compare different categories of data.

**Uses:**
- Comparing students' marks.
- Comparing sales of different products.
- Comparing the number of people in different groups.
 
  ```python
  plt.bar(df["Student"], df["Marks"])
  plt.title("Students' Mathematics Marks")
  plt.xlabel("Students")
  plt.ylabel("Marks")
  plt.show()

<img width="1468" height="480" alt="Screenshot 2026-11-05 at 10 04 53 AM" src="https://github.com/user-attachments/assets/a71d6bee-9d7d-49b0-a993-10f41817d112" />

<img width="691" height="546" alt="Screenshot 2026-11-05 at 10 07 45 AM" src="https://github.com/user-attachments/assets/5452fb57-d961-4d90-a930-3d4c1254212e" />


### B. Line Graph
A line graph uses points connected by lines to show changes over time.

**Uses:**
- Tracking temperature changes.
- Showing students' progress in tests.
- Observing changes in population over time.

  ```python
  tests = [1, 2, 3, 4, 5]
  marks = [55, 65, 70, 80, 90]

  plt.plot(tests, marks, marker="o")

  plt.title("Student's Progress")
  plt.xlabel("Test Number")
  plt.ylabel("Marks")

  plt.show()
  

### C. Pie Chart
A pie chart is a circular graph divided into sections. Each section represents a proportion of the whole.

**Uses:**
- Showing percentages.
- Representing how a budget is divided.
- Comparing different categories as parts of a whole.

### D. Histogram
A histogram represents the distribution of numerical data using bars. It helps us understand how frequently values occur within different ranges.

**Uses:**
- Understanding the distribution of students' marks.
- Analyzing age groups.
- Studying examination results.

## 5. Choosing the Right Graph

Different graphs are used for different purposes:

| Graph | Main Purpose |
|---|---|
| Bar Graph | Comparing categories |
| Line Graph | Showing changes over time |
| Pie Chart | Showing proportions or percentages |
| Histogram | Showing data distribution |

## 6. Conclusion

Data visualization is an important part of data analysis because it allows us to present information in a visual and understandable way. By using Python libraries such as Pandas and Matplotlib, we can create different graphs to explore data, identify patterns, and communicate our findings.
