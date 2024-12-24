

1. Data Preprocessing:
   - Started with a travel package dataset containing customer information and purchase outcomes
   - Handled missing values using:
     - Median imputation for Age, DurationOfPitch, and MonthlyIncome
     - Mode imputation for NumberOfChildrenVisiting, PreferredPropertyStar, and NumberOfFollowups
     - Dropped rows with missing values for NumberOfTrips and TypeofContact
   - Converted numeric columns to integer type
   - Fixed data quality issues (e.g., standardized "Fe Male" to "Binary" in Gender column)

2. Exploratory Data Analysis (EDA):
   - Created count plots for categorical variables (MaritalStatus, Gender, Designation, Occupation, ProductPitched)
   - Generated box plots to analyze relationships between:
     - DurationOfPitch, MonthlyIncome, NumberOfTrips vs ProdTaken
     - Various demographic features and purchase outcomes
   - Key visualizations included:
     - Number of followups vs Product Taken
     - Pitch satisfaction scores vs Product Taken
     - Monthly income distribution by city tier
     - Product purchase patterns across different customer segments

3. Statistical Analysis:
   - Performed Chi-square tests to analyze associations between:
     - Product Taken and categorical variables (Occupation, Gender, ProductPitched, Designation, MaritalStatus)
     - Found significant associations in most relationships
   - Conducted t-tests for numerical variables to compare means between customers who did/didn't purchase
   - Analyzed correlation patterns between features using Spearman correlation

4. Feature Engineering:
   - Applied One-Hot Encoding for categorical variables:
     - Occupation, Gender, ProductPitched, MaritalStatus, Designation
   - Used Label Encoding for TypeofContact
   - Standardized numerical features using StandardScaler
   - Performed Principal Component Analysis (PCA) to reduce dimensionality to 10 components

5. Model Development and Evaluation:
   - Built and evaluated three classification models:

   a. Decision Tree Classifier:
   - Used GridSearchCV for hyperparameter tuning
   - Implemented class balancing
   - Found optimal parameters for tree depth, splitting criteria, etc.

   b. Random Forest Classifier:
   - Selected important features (importance > 0.01)
   - Used RandomizedSearchCV for hyperparameter optimization
   - Balanced class weights
   - Tuned parameters including n_estimators, max_depth, min_samples_split

   c. AdaBoost Classifier:
   - Used Decision Tree as base estimator
   - Performed GridSearchCV for parameter tuning
   - Optimized learning rate and number of estimators
   - Evaluated using ROC-AUC scoring

6. Results:
   All models showed good performance with:
   - Random Forest achieving balanced accuracy between training and test sets
   - AdaBoost showing strong performance with optimized parameters
   - Decision Tree providing interpretable results with reasonable accuracy

The project successfully created a predictive model for travel package purchases, incorporating various aspects of customer data and using multiple modeling approaches to ensure robust predictions.
