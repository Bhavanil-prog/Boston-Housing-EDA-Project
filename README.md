# Boston-Housing-EDA-Project
This project provides a comprehensive Exploratory Data Analysis (EDA) of the Boston Housing Dataset. Exploratory Data Analysis (EDA) &amp; Regression Analysis

Boston Housing EDA Project Report
1. Project Type
Exploratory Data Analysis (EDA) & Regression Analysis

2. Project Prepared by
Bhavani L

3. Project Summary
This project provides a comprehensive Exploratory Data Analysis (EDA) of the Boston Housing Dataset. The primary goal is to identify and understand the key variables that influence the median value of owner-occupied homes (MEDV). The analysis follows a structured approach, starting from data collection and cleaning, and culminating in data visualization to reveal meaningful insights. This report is a foundation for anyone looking to understand the dataset's characteristics and prepare it for further machine learning modeling.

4. GitHub Link
[Your GitHub repository link here]

5. Problem Statement
The objective is to analyze the Boston Housing dataset to identify and explore the relationships between various features, such as crime rate (CRIM), number of rooms (RM), and pupil-teacher ratio (PTRATIO), and the target variable, MEDV. Through EDA, we aim to uncover patterns, distributions, and correlations that are crucial for building an accurate predictive model.

Coding Sections
Pre-processing of the Data
1. Import Libraries
This section imports all the necessary Python libraries for data manipulation, cleaning, and visualization.

Data Collection
Definition: This is the initial step where the dataset is loaded into a working environment, usually a Pandas DataFrame, to begin the analysis.

i) Data Set Loading
The dataset is loaded directly from the provided HousingData.csv file into a Pandas DataFrame.

Data Evaluation
Definition: After loading, the data is evaluated to understand its structure, identify missing values, and check for any data inconsistencies.

ii). Reading the Data
An initial look at the DataFrame's head and information provides a quick summary of the data, including column names, data types, and the presence of missing values.

iii). Data Set 1st Look
df.info() reveals the number of non-null values for each column, highlighting which ones have missing data that needs to be addressed.

3. Data Wrangling
Definition: This process involves cleaning and transforming raw data into a usable format for analysis. It includes handling missing values, fixing inconsistent entries, and removing duplicates.

i). Removing Exact Duplicates
The dataset is checked for any identical rows and duplicates are removed to ensure data integrity.

ii). Fixing Inconsistent Data Entries
The dataset is primarily composed of numerical data, so this step is not necessary.

iii). Handling Missing Values
Missing values are addressed by imputing them using the mean of each respective column. This ensures that no data points are lost and the dataset remains complete for analysis.

4. Detect and Treat the Outliers
Outliers are extreme values that can disproportionately affect the results of statistical analysis. The Interquartile Range (IQR) method is used here to identify and remove outliers in key features, such as LSTAT and MEDV, to create a more robust dataset.

5. Scaling and Normalization
This process scales the numerical features to a standard range. This is essential for many machine learning algorithms that are sensitive to the magnitude of feature values. StandardScaler is used to transform the data so that each feature has a mean of 0 and a standard deviation of 1.

6. Encoding Categorical Data
This is a step for datasets with non-numerical, categorical data. Since the Boston Housing dataset is entirely numerical (with the exception of CHAS, which is a dummy variable), a demonstration of One-hot Encoding is included to show how this step would work on a categorical feature if one were present.

7. Text Data
The dataset does not contain any text data, so this section is not applicable to this project.

8. Featuring Engineering
This is an advanced step where new features are created from existing ones to potentially improve the performance of a predictive model. This project will not perform any feature engineering.

9. Feature Selection / Reduce Dimensionality - PCA
Definition: Principal Component Analysis (PCA) is a technique used to reduce the dimensionality of the dataset by transforming a large set of variables into a smaller set of principal components while retaining as much information as possible.

10. Balance the Classes (classification Problem)
This step is only applicable to classification problems, where the number of data points for each class is imbalanced. Since this is a regression project, class balancing is not required.

Data Visualization
Correlation Heatmap
The heatmap below visualizes the correlation between all the variables in the dataset. A strong positive correlation is indicated by colors closer to red, while a strong negative correlation is shown by colors closer to blue.

Pair Plot
This plot displays the relationships between selected pairs of variables, such as LSTAT (lower status of the population) and MEDV (median home value), and RM (average number of rooms) and MEDV. The diagonal of the plot shows the distribution of each individual variable.

Scatter Plot with Regression Line
This plot specifically highlights the relationship between two variables, LSTAT and MEDV. The red regression line shows the trend, which is a clear negative correlation, indicating that as the percentage of lower-status population increases, the median home value tends to decrease.

PCA Scatter Plot
The final plot visualizes the data after dimensionality reduction using PCA. It shows the data points on the first two principal components, with the color of each point representing the median home value. This can help to visualize any clusters or patterns that exist within the data.
