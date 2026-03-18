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
