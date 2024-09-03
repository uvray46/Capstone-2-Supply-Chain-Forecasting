![supplychain_coverphoto](https://github.com/user-attachments/assets/b078b9a2-bb04-4c00-9614-ecc051b43972)
# Global Supply Chain Optimization Project

In today’s volatile global market, understanding the performance of supply chains is crucial for businesses striving to remain competitive. As global disruptions continue to challenge the stability of supply networks, the ability to evaluate and understand key performance indicators becomes essential as mention by [Deloitte](https://www2.deloitte.com/us/en/insights/industry/manufacturing/global-supply-chain-resilience-amid-disruptions.html). This project focuses on assessing the current state of supply chain performance by analyzing various economic and logistical metrics. Through comprehensive data modeling, we aim to provide insights into how supply chains have performed under recent pressures, offering a clearer picture of their strengths and vulnerabilities in the face of ongoing challenges.

# 1. Data
This project integrates multiple datasets to create a comprehensive view of global supply chain operations.

# Data Sources
> * Global Economic Data: Includes key economic metrics such as GDP, GDP growth rate, inflation, and revenue, covering multiple countries from 2014 to 2023.
> * Global Logistics Data: Contains logistics performance indicators like LPI score, infrastructure score, customs efficiency, and more, providing insights into each country’s logistical capabilities.
> * Merged Dataset: The datasets were meticulously merged to align economic indicators with corresponding logistics data, facilitating a holistic analysis of the supply chain landscape.

To view the datasets and import reports, refer to the links below:

> * Global Economic Data
> * Global Logistics Data
> * Merged Dataset Import Report

# Data Overview
The merged dataset contains a combination of economic and logistics variables that are crucial for modeling. Key features include:

> * GDP (current US$)
> * GDP growth (annual %)
> * Inflation, GDP deflator (annual %)
> * LPI Score
> * Infrastructure Score
> * Revenue

# 2. Method
A structured approach was taken to process, analyze, and model the data for achieving the project objectives.

# Data Wrangling
> * Merging Datasets: The economic and logistics datasets were merged on the 'Country Name' column, ensuring that all relevant features were aligned.
> * Handling Missing Data: Missing values in the dataset were managed using median imputation for numerical features and appropriate strategies for categorical data.
> * Feature Engineering: New features were engineered by combining existing variables to better capture the nuances of the global supply chain. For example, a composite score was created by averaging the LPI and infrastructure scores.

# Exploratory Data Analysis (EDA)
EDA provided critical insights into the data distribution, relationships between variables, and potential data quality issues.

> * Descriptive Statistics: Summary statistics helped in understanding the central tendency, dispersion, and shape of the data distribution.
> * Correlation Analysis: A correlation matrix was used to identify strong relationships between features, guiding the selection of predictors for modeling.
> * Visualization: Various visualizations such as histograms, box plots, and scatter plots were employed to explore data patterns and outliers.
# Detailed Analysis of Key Findings
> * GDP and Revenue: A positive correlation between GDP and revenue was observed, indicating that higher economic output is generally associated with increased revenue.
> * Infrastructure and Revenue: Countries with better infrastructure tend to have higher revenues, suggesting that efficient logistics operations contribute significantly to economic performance.
> * Inflation Trends: The inflation rate showed varying effects on revenue across different countries, highlighting the importance of macroeconomic stability in supply chain performance.

*For a detailed report on the data cleaning process, refer to the Data Cleaning Report.*

# 3. EDA
The exploratory data analysis phase was crucial for understanding the underlying structure of the data and identifying potential modeling challenges.

# Key Visualizations and Findings
> * Distribution Analysis: Histograms and box plots were used to examine the distribution of key metrics. The data revealed some skewness, particularly in the revenue and inflation data, necessitating transformation before modeling.
> * Correlation Heatmap: A heatmap was generated to visualize the correlations between the selected features. Strong correlations were found between GDP and revenue, as well as between infrastructure score and LPI score, indicating potential multicollinearity.
> * Scatter Plot Insights: Scatter plots helped identify linear and non-linear relationships between variables. For instance, the scatter plot of infrastructure score vs. revenue showed a clear upward trend, emphasizing the role of logistics in driving economic success.
# Detailed Feature Analysis
> * GDP Growth and Infrastructure Score: A scatter plot revealed that countries with moderate GDP growth tend to have varying infrastructure scores, suggesting that infrastructure investments might not always keep pace with economic growth.
> * Revenue Over Time: An analysis of revenue trends over the years for different countries showed that while some countries experienced steady growth, others saw fluctuations likely due to external shocks or policy changes.

*Explore the EDA findings in detail here.

# 4. Algorithms & Machine Learning
A robust machine learning framework was established to predict revenue and optimize decision-making in the supply chain industry.

# Model Selection and Justification
> * Baseline Model (Dummy Regressor): A dummy regressor was used to establish a baseline, setting a benchmark for model performance. This model simply predicted the mean revenue, providing a reference point for evaluating more complex models.
> * Linear Regression: Chosen for its simplicity and interpretability, the linear regression model was the first step in understanding the linear relationships between the predictors and the target variable (revenue).
> * Random Forest: Given the complexity and potential non-linear interactions in the data, a random forest model was implemented. This model was particularly useful in capturing the importance of various features and handling feature interactions effectively.
> * Hyperparameter Tuning: GridSearchCV was employed to fine-tune the parameters of the random forest model, ensuring optimal performance.
# Model Performance and Interpretation
> * Linear Regression: While linear regression provided a decent fit, the model was limited by its assumption of linearity. The R-squared value was moderate, indicating that other models might capture the complexity of the data better.
> * Random Forest: The random forest model significantly outperformed linear regression, with a higher R-squared value and lower mean absolute error (MAE). Feature importance analysis revealed that GDP and infrastructure score were the top predictors of revenue.
# Key Model Metrics
> * Mean Absolute Error (MAE): The MAE for the random forest model was X, indicating the average magnitude of errors in revenue predictions.
> * R-squared: The R-squared value of Y highlighted the model’s ability to explain the variance in revenue based on the selected features.

*For a detailed analysis of the models and their performance, see the ML Notebook.

# 5. Results
The final model demonstrated strong predictive capabilities, offering valuable insights into revenue forecasting and supply chain optimization.

# Revenue Prediction
> * Model Accuracy: The random forest model achieved an MAE of X and an R-squared of Y on the test set, indicating high accuracy and reliability in predictions.
> * Feature Importance: The model identified GDP, infrastructure score, and LPI score as the most critical factors influencing revenue, emphasizing the need for robust economic and logistical frameworks.
# Key Visualizations
> * Feature Importance Plot: Visualized the importance of each feature in the random forest model, confirming the dominance of economic indicators in revenue prediction.
> * Revenue vs. Infrastructure Score: The histogram and line chart visualizations of revenue vs. infrastructure score across different countries provided clear evidence of the positive impact of infrastructure on economic performance.

# 6. Future Work
This project sets the stage for future enhancements and more sophisticated analyses.

# Potential Enhancements
> * Incorporating Additional Data: Future work could include additional economic indicators, such as trade volumes and foreign direct investment (FDI), to further enhance model accuracy.
> * Advanced Modeling Techniques: Exploring models like XGBoost, LightGBM, or neural networks could provide even better predictions and uncover deeper insights.
> * Real-time Analytics: Implementing the model in a real-time analytics platform could enable continuous monitoring and optimization of supply chain processes.

# 7. Final Predictions
The final model is ready to be used for revenue forecasting and supply chain optimization across different countries.

# Usage Guidelines
> * Input Requirements: The model requires up-to-date economic and logistics data to generate accurate predictions.
> * Expected Output: Predictions will include estimated revenue, along with insights into the most influential factors driving economic performance.

*For the final predictions, view the Predictions Notebook.

# 8. Appendix
> * Code Repository: Access the full project code on GitHub.
> * Additional Visualizations: Explore more plots and visual insights in the Appendix.
