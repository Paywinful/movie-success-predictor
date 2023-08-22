# movie-success-predictor

## Movie Success Classification
### Introduction
This report offers a comprehensive analysis of a movie dataset, aiming to unravel valuable insights into movie attributes such as release year, revenue, ratings, directors, and actors. Our main objectives include data exploration, visualization of key relationships, and applying machine learning techniques to categorize movie success.
### Dataset Overview
The dataset under scrutiny contains crucial attributes like 'Title', 'Year', 'Revenue (Millions)', 'Rating', 'Director', 'Actors', and 'Metascore'. After importing the dataset into a Pandas DataFrame, rigorous preprocessing steps were undertaken to ensure data quality and reliability.
Exploratory Data Analysis
### Data Exploration
The initial phase involved a closer look at the dataset through the .info() function, which offered a snapshot of data types and the presence of any missing values. Additionally, the distribution and central tendencies of numerical attributes were explored using the .describe() function. The identification and handling of missing values were facilitated by the .isnull().sum() function.
### Data Preprocessing
To ensure data integrity, rows containing missing values were removed. Furthermore, the 'Genre' column, lacking relevance, was discarded. Additionally, the 'Year' column was converted to an integer data type to facilitate subsequent analysis.
### Data Visualization
A series of visualizations were employed to glean insights from the dataset:
A heatmap was constructed to visualize the correlation matrix, shedding light on potential connections among numerical variables.
Pie charts were used to highlight the most influential directors and actors within the dataset, providing a glimpse into the leading figures in the movie industry.
Scatter plots elucidated relationships between 'Year' and 'Revenue', 'Rating' and movie index, and 'Year' and total revenue, revealing trends and patterns.
### Metascore Analysis
The 'Metascore' attribute, representing critical reception, underwent an in-depth analysis. A function was devised to categorize 'Metascore' ratings into groups indicative of review sentiment. This resulted in the creation of a new column, 'Metascore Analysis'. The 'Metascore Analysis' section involves a thorough exploration of the 'Metascore' attribute, which reflects critical reviews. By categorizing Metascore ratings into groups based on sentiment, we gain insight into how movies are critically received. The resulting sentiment categories provide a nuanced understanding of critical perception, ranging from "Generally Unfavorable Reviews" to "Universal Acclaim." The subsequent bar plot visually communicates the distribution of these sentiment categories, offering a comprehensive overview of critical responses. Subsequently, a bar plot was employed to visualize the distribution of these sentiment categories.

## Classification Models
### Random Forest Classifier
For movie success classification, the Random Forest classifier emerged as a powerful tool. Utilizing features such as 'Year', 'Revenue (Millions)', and 'Rating', the dataset was divided into training and testing subsets. To standardize features, the StandardScaler was applied. Remarkably, the classifier demonstrated remarkable performance, achieving a training accuracy of 100% and a testing accuracy of approximately 99.4%. Importantly, the confusion matrix [[139 0], [1 28]] reaffirmed the classifier's capability in correctly categorizing instances.
### Support Vector Machine (SVM) Classifier
Parallelly, an SVM classifier with a linear kernel was introduced for the same classification task. Once again, the dataset was split, and features were standardized. The SVM classifier achieved a training accuracy of approximately 94.5% and a testing accuracy of around 91.1%. The corresponding confusion matrix [[136 3], [12 17]] validated the classifier's performance.

### The Multi-Layer Perceptron (MLP) Classifier
The Multi-Layer Perceptron (MLP) Classifier adds depth to the analysis, introducing a new dimension to the classification task. Alongside previous methodologies, the dataset is divided into training and testing subsets with standardized features. The MLP classifier exhibits exceptional performance, achieving a 100% training accuracy and approximately 92.2% testing accuracy, showcasing its ability to capture intricate patterns and generalize insights. The derived confusion matrix [[135 4], [9 20]] attests to its efficacy in accurately discerning between successful and less successful movies. This integration enriches the study's perspective, highlighting the synergy between advanced machine learning techniques and cinematic data, emphasizing the potential of predictive analytics in the film industry.
### Confusion Matrix Interpretation
The confusion matrix for the Random Forest classifier indicates that among the True Positive (TP) cases (actual success predicted as success), there were 139 instances. There were no False Negatives (FN) (actual success predicted as failure), and only one False Positive (FP) (actual failure predicted as success). Additionally, 28 instances were True Negatives (TN) (actual failure predicted as failure).
In the SVM classifier's confusion matrix, there were 136 True Positives (TP), 3 False Positives (FP), 12 False Negatives (FN), and 17 True Negatives (TN). This signifies that 136 instances of actual success were correctly predicted, while 12 actual successes were incorrectly predicted as failures.
The derived confusion matrix [[135 4], [9 20]] for the MLP classifier affirms its efficacy in accurately discerning between successful and less successful movies. With 135 true positives and 20 true negatives, the classifier demonstrates its ability to correctly classify both categories. Additionally, the minimal instances of false positives (4) and false negatives (9) underscore the classifier's precision in predictive tasks, contributing to its overall effectiveness in classification.

## Conclusion
This all-encompassing analysis illuminated the intricacies of the movie dataset, uncovering crucial insights through thorough exploration, impactful visualization, and effective classification. Notably, the Random Forest classifier exhibited superior accuracy in classifying movie success compared to the SVM classifier. This underlines its prowess in leveraging essential features for accurate predictions based on select attributes.


