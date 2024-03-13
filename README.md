# Heart Failure Prediction
[View Notebook for code and visalisations](https://github.com/prottayislive/Heart-Failure-Prediction-Analysis/blob/main/Heart_Failure_Prediction.ipynb)
## Introduction
This project aims to predict heart failure using clinical features through various machine learning models. Heart failure is a common, costly, and potentially fatal condition, and early prediction can significantly improve outcomes. The analysis, conducted in a Jupyter notebook, employs a dataset containing several clinical features indicative of heart health.

## Data Description
The dataset includes clinical records of patients, featuring key indicators such as age, blood pressure, cholesterol levels, heart rate, and other vital signs. These features are utilized to predict the likelihood of heart failure in patients.

## Methodology

### Data Preprocessing
- **Data Cleaning**: Initial steps involved handling missing values and removing outliers to ensure the quality of the dataset.
- **Feature Selection**: Key features were selected based on their relevance and impact on heart failure, as determined by domain knowledge and preliminary analysis.
- **Normalization**: Data normalization was applied to scale the features, making the dataset suitable for machine learning algorithms that are sensitive to the scale of input data.

### Exploratory Data Analysis (EDA)
- **Distribution Analysis**: Plots such as histograms and boxplots were generated to understand the distribution of key features. These visualizations helped identify skewness in the data and potential outliers.
- **Correlation Analysis**: Correlation matrices were used to identify relationships between different clinical features. Heatmaps visualizing these correlations provided insights into which features are most related to the risk of heart failure.
- **Feature Importance**: Techniques such as PCA (Principal Component Analysis) were used to identify and visualize the most significant features contributing to heart failure.

### Model Building and Evaluation
Several machine learning models were implemented and evaluated:
- **Decision Trees and Random Forest**: Provided insights into feature importance and allowed for a non-linear approach to classification.

### Decision Tree Analysis
The Decision Tree model was evaluated at various depths to understand its performance concerning overfitting and generalization capabilities. Here's a summary of its performance metrics:

- At a depth of 1, the model achieves a balance between training and test accuracy (85.65% and 82.22%, respectively), with a cross-validation (CV) accuracy of 84.70%, suggesting a simplistic model that generalizes well but might be underfitting.
- Increasing the depth to 3 improves the training accuracy to 89.00% but slightly decreases test accuracy to 78.89%, with CV accuracy dropping to 78.97%, indicating the onset of overfitting.
- At a depth of 8, the training accuracy reaches 100%, indicating perfect fitting on the training data. However, test accuracy plateaus at 77.78%, and CV accuracy drops to 74.63%, clearly showing overfitting where the model fails to generalize well to unseen data.

### Random Forest Analysis
The Random Forest model, known for its ensemble learning capability to reduce overfitting, was also evaluated across various depths:

- At lower depths (1-2), the model demonstrates decent generalizability, with test accuracies of 72.22% and 80.00%, respectively. The CV accuracy at depth 2 is 81.36%, indicating a robust model against overfitting at this stage.
- Increasing the depth to 4 and 5 sees improvements in both training and test accuracies, peaking at 94.26% and 85.56% for training and test datasets, respectively, with a CV accuracy of 85.18% at depth 4.
- Beyond depth 5, while training accuracy continues to improve, reaching 100% at depth 7, test accuracy and CV accuracy do not significantly increase, suggesting that the model gains from additional depth diminish.

### Key Insights
- **Decision Tree vs. Random Forest**: The Random Forest model outperforms the Decision Tree in test accuracy and shows better resistance to overfitting, thanks to its ensemble approach.
- **Optimal Complexity**: Both models exhibit optimal performance at a medium complexity level (depth 3-5 for Decision Trees and depth 4-5 for Random Forest). Beyond these points, improvements in training accuracy come at the cost of generalization.
- **Generalization Capability**: The Random Forest model demonstrates a superior ability to generalize across different depths, with its ensemble method effectively managing the bias-variance trade-off.

## Key Findings and Visualizations
- **Risk Factors**: Visualizations from EDA highlighted significant risk factors for heart failure, such as elevated blood pressure and cholesterol levels.
- **Model Performance**: Among the models evaluated, Random Forest and Neural Networks showed promising results, achieving high accuracy and precision.
- **Feature Importance**: Decision tree-based models revealed that certain features, like age and ejection fraction, were particularly predictive of heart failure.

## Conclusion
The project successfully demonstrates the application of machine learning models to predict heart failure from clinical features. The findings underscore the importance of early detection and the potential for machine learning to assist in diagnostic processes. Future work could explore more advanced models, feature engineering techniques, and larger datasets to further improve prediction accuracy.

## Implications and Future Directions
- **Clinical Application**: These models can assist healthcare professionals in identifying high-risk patients for early intervention.
- **Model Improvement**: Future analyses could incorporate additional data sources, more complex models, and techniques like cross-validation to enhance predictive performance.
- **Feature Engineering**: Investigating more sophisticated feature engineering methods could uncover deeper insights and improve model accuracy.

This report encapsulates the process and findings of the Heart Failure Prediction project, highlighting the potential of machine learning in transforming healthcare analytics and patient care strategies.

---
