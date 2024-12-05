### Weekly Learning Objectives:

- By the end of this lesson, students will be able to load and inspect a dataset using Python's Pandas library to assess initial data integrity.
- By the end of this lesson, students will be able to identify and address common data issues, such as duplicates, incorrect data types, and inconsistent formatting.
- By the end of this lesson, students will be able to standardize and transform categorical and binary data for analytical use.
- By the end of this lesson, students will be able to document assumptions, cleaning steps, and transformations during the data preparation process.
- By the end of this lesson, students will be able to analyze and answer specific questions using a cleaned dataset, applying EDA techniques to derive insights.

### Sample Questions and Answers:

1. Question: How would you load a dataset in Python and view its initial structure?  
   Answer: I would use Pandas to load the dataset, for example, with `pd.read_excel()` if it's an Excel file. To check the initial structure, I would use `df.head()` to preview the first few rows, `df.columns` to list column names, and `df.dtypes` to check data types.

2. Question: Describe a common data inconsistency you might encounter with categorical variables and how to handle it.  
   Answer: A common inconsistency is varied representations for the same category, such as "Yes," "Y," "1," and "True" for a binary variable. I would standardize these into a consistent format, such as 1s and 0s, using conditional replacement or by applying a function to convert these values.

3. Question: When preparing data, why is it essential to document each transformation step?  
   Answer: Documenting each step ensures transparency and reproducibility, allowing others (or myself in the future) to understand the assumptions, corrections, and transformations applied. It also helps in troubleshooting or revisiting the dataset if issues arise later.

4. Question: What graphical techniques might you use in EDA to detect data patterns or outliers?  
   Answer: Techniques like scatter plots, box plots, and histograms are useful for visualizing relationships, distribution patterns, and detecting outliers in data, providing insights that might be overlooked in raw data tables.

5. Question: How would you approach answering the question, "Which operator had the most spills?"  
   Answer: I would use `value_counts()` on the operator column to count the number of spills per operator. If there were naming inconsistencies (e.g., different formats for the same operator), I would clean these first to ensure accurate counts.

These objectives and questions are structured to reinforce students' understanding of essential EDA tasks, data preparation, and analytical insight techniques using Python.