# Lesson 5 — Data Analysis Project

## 1. Introduction

In this lesson, I will apply the Python skills I have learned to complete a real-world data analysis project.

For this project, I will use a **Student Performance Dataset** from Kaggle to explore students' academic performance and identify patterns in their results.

## 2. Project Objectives

The main objectives of this project are:

- Understand and explore the dataset.
- Clean the data by handling missing values and duplicates.
- Calculate the average student performance.
- Identify the highest and lowest scores.
- Explore patterns in students' performance.
- Create graphs to visualize the results.
- Draw conclusions based on the data.

## 3. Dataset Information

**Dataset:** Student Performance Dataset

**Source:** Kaggle

**Tools Used:**
- Python
- Google Colab
- Pandas
- Matplotlib

The dataset contains information about students and their academic performance.

## 4. Loading the Dataset

First, I will import Pandas and load the dataset into Google Colab.

<img width="1439" height="411" alt="Screenshot 2026-11-05 at 11 07 09 AM" src="https://github.com/user-attachments/assets/c2895d20-2cc6-4531-b0a8-b46c68ccf84a" />


## 5. Exploring the Dataset

I will explore the dataset to understand its structure and information.



https://github.com/user-attachments/assets/9a94cb75-d2a5-4216-bd2e-dcc5664b5add



## 6. Cleaning the Data

Before analyzing the dataset, I will check for missing values and duplicate records.

```python
# Check missing values
print(df.isnull().sum())

# Remove duplicate records
df = df.drop_duplicates()

# Check the dataset again
print(df.shape)
```

## 7. Analyzing the Data

I will calculate the average scores and identify patterns in students' academic performance.

```python
# Calculate average mathematics score
print("Average Math Score:", df["math score"].mean())

# Calculate average reading score
print("Average Reading Score:", df["reading score"].mean())

# Calculate average writing score
print("Average Writing Score:", df["writing score"].mean())
```

## 8. Data Visualization

I will use graphs to make the results easier to understand.

```python
import matplotlib.pyplot as plt

# Calculate average scores
averages = [
    df["math score"].mean(),
    df["reading score"].mean(),
    df["writing score"].mean()
]

subjects = ["Math", "Reading", "Writing"]

plt.bar(subjects, averages)

plt.title("Average Student Performance")
plt.xlabel("Subjects")
plt.ylabel("Average Marks")

plt.show()
```

## 9. Conclusion

After completing this project, I will be able to understand how data analysis works using a real dataset.

I will use the results and graphs to identify patterns in students' academic performance and draw conclusions from the information.

This project will help me improve my Python programming, data cleaning, data analysis, and visualization skills.





