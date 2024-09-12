# Portfolio-RStudio

**Repository for Data Analyis on Iris:**
This repository contains code and analysis related to data analysis and data visualization using R Studio.
Project: Iris Dataset Cleaning and Visualization

**Dataset:**

The Iris dataset contains measurements of sepal length, sepal width, petal length, and petal width for 150 iris flowers from three species: setosa, versicolor, and virginica.

### **Data Exploration and Analysis**

**Exploratory Data Analysis (EDA):**

* **Histograms:** Visualize the distribution of sepal length, sepal width, petal length, and petal width.
* **Scatter Plots:** Examine relationships between features.
* **Box Plots:** Compare the distributions of petal length and petal width across species.

**Hypothesis Testing:**

* **ANOVA:** Conduct an ANOVA test to determine if there are significant differences in sepal length among the species.

**Correlation Analysis:**

* Calculate correlation coefficients between sepal length, sepal width, petal length, and petal width.

**Code:**

```R
library(ggplot2)

# Load the Iris dataset
data(iris)

# Histogram of sepal length
ggplot(iris, aes(x = Sepal.Length)) +
  geom_histogram() +
  labs(title = "Sepal Length Distribution")

# Scatter plot of sepal length vs. sepal width by species
ggplot(iris, aes(x = Sepal.Length, y = Sepal.Width, color = Species)) +
  geom_point() +
  labs(title = "Sepal Length vs. Sepal Width by Species")

# Box plot of petal length by species
ggplot(iris, aes(x = Species, y = Petal.Length)) +
  geom_boxplot() +
  labs(title = "Petal Length by Species")

# ANOVA test
model <- aov(Sepal.Length ~ Species, data = iris)
summary(model)

# Correlation matrix
correlation_matrix <- cor(iris[, 1:4])
print(correlation_matrix)
```

### **Results**

* **ANOVA:** The ANOVA test shows that there are significant differences in sepal length among the three species (p-value < 2e-16).
* **Correlation:** The correlation matrix reveals strong positive correlations between sepal length and petal length, as well as between sepal width and petal width. There are negative correlations between sepal length and sepal width, and between petal length and petal width.

### **Conclusions**

Based on the analysis, we can conclude that sepal length is a significant factor in distinguishing the iris species. Additionally, the strong correlations between sepal length and petal length, as well as between sepal width and petal width, suggest that these features are interrelated.




**Repository for Data Cleaning Iris Dataset:**
This repository also contains R code for cleaning and visualizing the Iris dataset, a classic dataset used in machine learning. 
The code performs tasks such as handling missing values, converting data types, and removing outliers.

**Requirements:**

RStudio
tidyverse package
Usage:

Clone this repository to your local machine.
Open the R Markdown file iris_cleaning.Rmd in RStudio.
Knit the document to generate an HTML or PDF output.
Code Structure:
The Data CLeaning Iris Dataset.Rmd file includes the following sections:

**Data Loading: Loads the Iris dataset.**
Data Exploration: Provides basic information about the dataset.
Data Cleaning: Handles missing values, converts data types, and removes outliers.
Data Visualization: Creates a histogram of sepal length.
Results
The cleaned dataset is saved as cleaned_iris. The histogram shows the distribution of sepal lengths after outlier removal.

 
