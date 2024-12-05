### Weekly Learning Objectives

By the end of this lesson, students will be able to:

1. Perform data grouping using the split-apply-combine workflow with pandas `groupby` to summarize and analyze datasets effectively.
2. Apply custom aggregation functions to grouped data, leveraging pandas' `aggregate` method for complex multi-function analyses.
3. Use transformations on grouped data to normalize values, create derived columns, or segment data for detailed trend analysis.
4. Create and interpret pivot tables and cross-tabulations to summarize and visualize relationships in multi-dimensional datasets.
5. Develop advanced group-wise analyses, such as calculating weighted averages, group-specific correlations, or applying statistical models to grouped data.

---

### Questions and Answers to Assess Learning Objectives

#### **Objective 1: Grouping with Split-Apply-Combine**

**Question:**  
Explain the split-apply-combine workflow and demonstrate how to calculate the average value of a column grouped by another column in a DataFrame.

**Answer:**  
The split-apply-combine workflow involves:
1. **Split:** Dividing the data into groups based on a key (e.g., a column value).  
2. **Apply:** Performing computations or transformations on each group independently.  
3. **Combine:** Merging the results into a new DataFrame or Series.

**Example Code:**
```python
import pandas as pd

data = pd.DataFrame({
    'Category': ['A', 'B', 'A', 'B', 'C'],
    'Values': [10, 20, 30, 40, 50]
})

# Group by 'Category' and calculate the mean of 'Values'
result = data.groupby('Category')['Values'].mean()
print(result)
```
**Output:**
```
Category
A    20.0
B    30.0
C    50.0
```

---

#### **Objective 2: Custom Aggregations**

**Question:**  
How can you calculate both the mean and sum of a column for each group in a pandas DataFrame?

**Answer:**  
Using the `aggregate` method:
```python
# Aggregate mean and sum for each group
result = data.groupby('Category')['Values'].aggregate(['mean', 'sum'])
print(result)
```
**Output:**
```
          mean  sum
Category           
A         20.0   40
B         30.0   60
C         50.0   50
```

---

#### **Objective 3: Transformations**

**Question:**  
What is the difference between `apply` and `transform` when working with grouped data? Provide an example of using `transform` to normalize values within each group.

**Answer:**  
- `apply` returns a reduced or aggregated result, while `transform` returns an output of the same shape as the input.
- `transform` is often used for group-wise transformations, such as normalization.

**Example Code:**
```python
# Normalize 'Values' by subtracting the group mean
data['Normalized'] = data.groupby('Category')['Values'].transform(lambda x: (x - x.mean()))
print(data)
```
**Output:**
```
  Category  Values  Normalized
0        A      10       -10.0
1        B      20       -10.0
2        A      30        10.0
3        B      40        10.0
4        C      50         0.0
```

---

#### **Objective 4: Pivot Tables and Cross-Tabulations**

**Question:**  
Create a pivot table to show the sum of values grouped by two columns: `Category` and a new column `Subgroup`.

**Answer:**  
```python
# Add a Subgroup column
data['Subgroup'] = ['X', 'Y', 'X', 'Y', 'X']

# Create a pivot table
pivot = data.pivot_table(values='Values', index='Category', columns='Subgroup', aggfunc='sum', fill_value=0)
print(pivot)
```
**Output:**
```
Subgroup     X   Y
Category           
A           40   0
B            0  60
C           50   0
```

---

#### **Objective 5: Advanced Group-Wise Analysis**

**Question:**  
Demonstrate how to calculate a weighted average for a grouped DataFrame.

**Answer:**  
```python
# Add weights column
data['Weights'] = [1, 2, 3, 4, 5]

# Calculate weighted average
def weighted_avg(group):
    return (group['Values'] * group['Weights']).sum() / group['Weights'].sum()

result = data.groupby('Category').apply(weighted_avg)
print(result)
```
**Output:**
```
Category
A    23.333333
B    35.000000
C    50.000000
dtype: float64
```