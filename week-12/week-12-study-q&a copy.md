### Weekly Learning Objectives:

By the end of this lesson, students will be able to:

1. Create and customize static visualizations using `matplotlib`, including adjusting figure properties, axes, and subplots to effectively present data.  
2. Use `seaborn` to create and interpret statistical plots, such as regression lines, bar plots, and heatmaps, to uncover and display relationships within data.  
3. Evaluate and implement principles of effective data visualization to create "data-ink-rich" graphics while avoiding misleading elements.  
4. Integrate visualizations into analytical narratives to support data-driven conclusions effectively.  
5. Compare the capabilities of different Python visualization libraries (e.g., `matplotlib`, `seaborn`, `plotly`, `Bokeh`) and choose appropriate tools for static and interactive visualizations.

---

### Questions to Assess Learning Objectives

#### **Objective 1: Static Visualizations with `matplotlib`**  
**Question:**  
How would you create a figure with two subplots arranged horizontally, where the first subplot shows a bar chart and the second a scatter plot? Customize the figure to include grid lines in both subplots.

**Answer:**  
```python
import matplotlib.pyplot as plt

# Create figure and subplots
fig, axes = plt.subplots(1, 2, figsize=(10, 5))

# Bar chart in the first subplot
axes[0].bar(['A', 'B', 'C'], [10, 20, 15])
axes[0].set_title('Bar Chart')
axes[0].grid(True)

# Scatter plot in the second subplot
axes[1].scatter([1, 2, 3], [3, 5, 7])
axes[1].set_title('Scatter Plot')
axes[1].grid(True)

# Display the plot
plt.tight_layout()
plt.show()
```

---

#### **Objective 2: Statistical Plots with `seaborn`**  
**Question:**  
Using `seaborn`, how would you create a heatmap to visualize the correlation matrix of a dataset? Add annotations to display the correlation values.

**Answer:**  
```python
import seaborn as sns
import pandas as pd

# Example dataset
data = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6],
    'C': [7, 8, 9]
})

# Calculate correlation matrix
corr = data.corr()

# Create heatmap
sns.heatmap(corr, annot=True, cmap='coolwarm')
plt.title('Correlation Heatmap')
plt.show()
```

---

#### **Objective 3: Principles of Effective Visualization**  
**Question:**  
What are three principles of effective data visualization according to Edward Tufte, and how would you apply them in a Python plot?

**Answer:**  
- **Principle 1:** Minimize "chart junk" by avoiding unnecessary elements like excessive grid lines or background colors.  
- **Principle 2:** Maximize the "data-ink ratio" by focusing on the data and removing irrelevant details.  
- **Principle 3:** Use colors and labels judiciously to enhance clarity.  

**Application in Python:**  
```python
plt.plot([1, 2, 3], [10, 20, 15], marker='o', label='Trend Line')
plt.title('Effective Visualization')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.legend()
plt.grid(False)  # Removing grid lines to minimize chart junk
plt.show()
```

---

#### **Objective 4: Integrating Visualizations with Analysis**  
**Question:**  
When integrating visualizations into a data analysis report, what are three practices to ensure they effectively support your analytical narrative?

**Answer:**  
1. **Provide Context:** Include captions and titles that explain the visualization's purpose.  
2. **Focus on Key Insights:** Highlight the most important data points or trends using annotations or markers.  
3. **Align with Narrative:** Ensure the visualization directly supports and aligns with the text's argument or analysis.

---

#### **Objective 5: Comparing Visualization Libraries**  
**Question:**  
What are the primary differences between `matplotlib`, `seaborn`, and `plotly`, and when would you use each?

**Answer:**  
- **`matplotlib`:** Best for basic and highly customizable static plots. Use it for fine-grained control over plot elements.  
- **`seaborn`:** Built on `matplotlib` with enhanced aesthetics and simpler syntax for statistical visualizations. Use it for creating regression plots, heatmaps, or pair plots.  
- **`plotly`:** Ideal for creating interactive and web-based visualizations. Use it for dashboards or when interactivity (e.g., zooming) is required.