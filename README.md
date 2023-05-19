# Online-Payment-Fraud-Detection
This is a machine learning model that is used to predict online payment fraud
for Blossom Bank

The aim of the bank project is to utilize machine learning techniques for predicting fraudulent banking transactions. The dataset consists of over 1,000,000 entries across various categories, organized in a CSV file format that includes both categorical and non-categorical variables.

To evaluate the data, I followed a systematic approach comprising several steps: data exploratory analysis (EDA) and visualization, feature engineering, model selection, and training and evaluation.

During the EDA phase, I conducted a thorough analysis and visualization of the data. One notable finding was the absence of missing data, as confirmed through null and descriptive analyses. Furthermore, within the categorical variable "type," there were five transaction types: Cash_in, Cash_out, Debit, Payment, and Transfer. Among these transaction types, only Cash_out and Transfer exhibited instances of fraudulent transactions. However, the total number of fraudulent transactions in both categories was less than 0.2% of the overall transactions. Additionally, the median value associated with fraudulent transactions was found to be insignificant.

In order to capture the relationships between key categorical variables and the "isFraud" label, I employed various visualizations such as bar charts, heatmaps, and pair plots. Moreover, I conducted univariate and multivariate analyses to explore the connections between categorical variables and other important features.

For effective model testing, training, and prediction, I performed feature engineering by encoding the data. This process involved dropping certain categorical variables ("nameOrig" and "nameDest") from the DataFrame and generating dummy variables using Python syntax. To select the appropriate model, I considered "isFraud" as the primary categorical variable, denoting it as 'y' and excluding it from the remaining DataFrame. I then proceeded to evaluate different models, including RandomForest, DecisionTree, KNeighbor, and LogicRegression. In order to assess the models' performance, I utilized a confusion matrix to analyze false negatives and true positives.

Based on the analysis, I observed that both Random Forest and KNeighbor demonstrated better predictive capabilities in detecting fraudulent transactions compared to the other models. However, I recommend utilizing Random Forest due to its higher precision of 98% compared to KNeighbor's 78%, as well as its superior recall rate of 79% versus 50% for KNeighbor. Additionally, the F1-score for Random Forest was 87%, while KNeighbor achieved a score of 61%.

One significant challenge encountered during the project was encoding the data due to the large dataset size and limitations of my system's capacity to process it efficiently.

To overcome this challenge, I made the decision to drop two categorical variables from the main DataFrame, which helped alleviate the encoding difficulties
To overcome this challenge, I made the decision to drop two categorical variables from the main DataFrame, which helped alleviate the encoding difficulties.
