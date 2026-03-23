# Project 2 - When Will a Power Outage Occur?
## Software 

Primary Software: Jupyter Notebook  
  
Add-on Packages: 
- pandas
- matplotlib.pyplot
- seaborn
- os 
- numpy
- make_regression (from sklearn.datasets)
- train_test_split, KFold, cross_val_score (from sklearn.model_selection)
- LinearRegression (sklearn.linear_model)
- RandomForestRegressor, GradientBoostingRegressor (from sklearn.ensemble)
- r2_score, mean_absolute_error, mean_squared_error (from sklearn.metrics)
- StandardScaler (from sklearn.preprocessing)
- GridSearchCV, RandomizedSearchCV (from sklearn.model_selection)

Platform: macOS

## Documentation Map

```
Data/
├── cleaned_data.csv
└── initial_data.csv

Outputs/
├── EDA/
│   ├── distribution_of_outages_by_hour.jpg
│   ├── distribution_of_outages_by_type.jpg
│   ├── frequency_of_outages_by_month.jpg
│   └── top_ten_states_by_month.jpg
└── performance_table.png

Scripts/
├── EDA.ipynb
├── cleaning.ipynb
└── model_and_analysis.ipynb

.gitignore
License
README.md
```

## Instructions for Reproduction
#### Pre-Cleaning  
- Download the required packages
#### Cleaning  
1. Upload the dataset initial_data.csv 
2. Drop columns "state_event", "Datetime Event Began", "Datetime Restoration", "fips", "min_customers", "max_customers" and "mean_customers"
3. Create a column for hour by converting start_time into a datetime object for hour
4. Save to a new csv (cleaned_data.csv)
#### EDA  
1. Upload the dataset cleaned_data.csv
2. Convert start_time and end_time columns to datatime objects
3. Extract month and hour
4. Set month order 
5. Create a graph of the distribution of top ten states affected by outages by month and save as an image to the outputs folder on Github
6. Create a graph of the frequency of outages by month and save as an image to the outputs folder on Github
7. Create a graph of the distribution of outages by event_type and save as an image to the outputs folder on Github
8. Create a graph of the distribution of the time of day outage began and save as an image to the outputs folder on Github
9. Create a graph of the distribution of the duration of outages and save as an image to the outputs folder on Github
#### Data Analysis  
1. Convert start_time to datetime object
2. Extract month, day of the week, and day
3. Create a feature matrix and define y variable
4. Split data into train and test set
5. Scale data and convert back to a dataframe
6. Define cross-validation 
7. Run a linear regression model on data and test R^2, Mean Absolute Error, and Root Mean Squared Error
8. Run a random forest model on data and test R^2, Mean Absolute Error, and Root Mean Squared Error
9. Run an XGBoost model on data and test R^2, Mean Absolute Error, and Root Mean Squared Error
10.
### Hyperparameter Tuning 
1. Rerun linear regression model, but add tuning in order to test model performance  
    a. Test R^2 score, Mean Absolute Error, and Root Mean Squared Error
2. Rerun random forest model, but add tuning in order to test model performance  
    a. Test R^2 score, Mean Absolute Error, and Root Mean Squared Error
3. Rerun XGBoost model, but add tuning in order to test model performance  
    a. Test R^2 score, Mean Absolute Error, and Root Mean Squared Error 
#### Model Evaluation  
1. Define variables for metrics table
2. Define models for metrics table
3. Create a metrics tabel to compare the R^2 score, Mean Absolute Error score, and Root Mean Sqaured Error score of all three models before and after hyperparameter tuning  
     a. Save as an image to the outputs folder on Github


## Note

The dataset in which we used for this project includes a disclaimer concerning the contents of the data. The most recent version of the disclaimer is uploaded to this repository, but in the case that the disclaimer changes, it can be found here: https://catalog.data.gov/dataset/event-correlated-outage-dataset-in-america
