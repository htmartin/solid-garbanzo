### **Weekly Learning Objectives**

By the end of this week, students will be able to:

1. Create and manipulate pandas Series and DataFrames to represent and analyze tabular data efficiently.
2. Apply operations such as indexing, filtering, and sorting to extract and transform data within pandas structures.
3. Use pandas methods, such as `apply`, `agg`, and `applymap`, to compute statistics and apply custom functions across Series and DataFrames.
4. Perform arithmetic operations and handle missing data in pandas, leveraging automatic alignment and broadcasting features.
5. Generate visualizations directly from pandas DataFrames and save data to and load data from files (e.g., CSV) for data persistence and sharing.

---

### Study Questions 

#### **1. Creating and Manipulating pandas Series and DataFrames**
- **Question**: Write Python code to create a pandas DataFrame with columns "Name", "Age", and "Score". Add a new column "Passed" that indicates whether the "Score" is greater than or equal to 50.  
  **Answer**:  
  ```python
  import pandas as pd

  data = {
      "Name": ["Alice", "Bob", "Charlie"],
      "Age": [25, 30, 35],
      "Score": [45, 75, 60]
  }

  df = pd.DataFrame(data)
  df["Passed"] = df["Score"] >= 50

  print(df)
  ```
  **Output**:  
  ```
      Name  Age  Score  Passed
  0  Alice   25     45   False
  1    Bob   30     75    True
  2 Charlie   35     60    True
  ```

---

#### **2. Indexing, Filtering, and Sorting**
- **Question**: How can you select rows in a DataFrame where the "Age" column is greater than 28? Sort the resulting DataFrame by "Score" in descending order.  
  **Answer**:  
  ```python
  filtered = df[df["Age"] > 28]
  sorted_df = filtered.sort_values(by="Score", ascending=False)

  print(sorted_df)
  ```
  **Output**:  
  ```
      Name  Age  Score  Passed
  1    Bob   30     75    True
  2 Charlie   35     60    True
  ```

---

#### **3. Applying Functions**
- **Question**: Use `apply` to compute a "Category" column in the DataFrame based on the "Score" column. Scores ≥ 70 should be labeled "High", scores ≥ 50 as "Medium", and others as "Low".  
  **Answer**:  
  ```python
  def categorize(score):
      if score >= 70:
          return "High"
      elif score >= 50:
          return "Medium"
      else:
          return "Low"

  df["Category"] = df["Score"].apply(categorize)

  print(df)
  ```
  **Output**:  
  ```
      Name  Age  Score  Passed Category
  0  Alice   25     45   False      Low
  1    Bob   30     75    True     High
  2 Charlie   35     60    True   Medium
  ```

---

#### **4. Handling Missing Data and Arithmetic Operations**
- **Question**: Write Python code to create a DataFrame with missing values. Fill missing values in the "Score" column with the mean of the column.  
  **Answer**:  
  ```python
  data = {
      "Name": ["Alice", "Bob", "Charlie"],
      "Age": [25, None, 35],
      "Score": [45, 75, None]
  }

  df = pd.DataFrame(data)
  df["Score"] = df["Score"].fillna(df["Score"].mean())

  print(df)
  ```
  **Output**:  
  ```
      Name   Age  Score
  0  Alice  25.0   45.0
  1    Bob   NaN   75.0
  2 Charlie  35.0   60.0
  ```

---

#### **5. Visualizing and Saving Data**
- **Question**: Plot a histogram of the "Score" column and save the DataFrame to a CSV file.  
  **Answer**:  
  ```python
  import matplotlib.pyplot as plt

  df["Score"].hist()
  plt.title("Score Distribution")
  plt.xlabel("Score")
  plt.ylabel("Frequency")
  plt.show()

  df.to_csv("data.csv", index=False)
  print("DataFrame saved to 'data.csv'")
  ```
  **Output**: Displays a histogram and saves the DataFrame to a CSV file.

---

