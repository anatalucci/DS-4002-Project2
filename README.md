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
1. Clean data to remove uppercase characters, non-word characters, extra whitespace
2. Remove reviews with 3-star reviews
3. Save to a new csv (filtered_firestick_reviews.csv)
4. Create a copy of the dataset and create binary labeling for the star-ratings (1 for 4-5 stars, 0 for 1-2 stars)
5. Save to new csv as a column
6. Create a data frame to combine the text in the columns "text" and "title"
7. Set the maximum words and maximum length based on the number of rows and length of text
8. Tokenize the text by replacing words that are not in the vocab and assign integers to words
9. Convert sequences of text into sequences of integers and pad the sequences to be the same length
10. Create two train splits: one with stratification and one without stratification  
11. Build the text CNN to classify the reviews  
    a. Set the size of each word vectors and define the input to be a sequence of integers with size maximum length  
    b. Create three convulations with different kernel sizes (3, 4, 5)  
    c. Create three pools to reducde the size of each input (based on each convolution)  
    d. Combine the pooled inputs, create a dropout layer to prevent overfitting and define outputs with sigmoid-activation to output predicted class  
    e. Define the model with binary cross-entropy loss, the adam optimizer, and accuracy metric  
    f. Save a visualization of the model as an image to outputs folder  
12. Train the model on the train split for 30 epochs (one for the stratified and one for the nonstratified)
13. Create two confusion matrices (one for stratified and one for nonstratified)  
    a. Save the plots as images to outputs folder
14. Create two metrics tables (one for stratified and one for nonstratified)  
    a. Report accuracy, precision, recall, f1, and binary cross-entropy  
    b. Save the two metrics tables as images to the outputs folder  
#### Mitigating the Class Imbalance  
1. Get the indices for each class
2. Ensure equal sizes of the classes and randomly sample an equal amount from each class (positive and negative)
3. Combine and shuffle the samples
4. Create a new set
5. Create a new train split with the balanced data
6. Clone and apply the model to the balanced split
7. Create a confusion matrix for the balanced data  
     a. Save the matrix as an image to outputs folder
8. Create a metric table for the balanced data, reporting same metrics  
     a. Save as an image to outputs folder 


## Note

The dataset in which we used for this project includes a disclaimer concerning the contents of the data. The most recent version of the disclaimer is uploaded to this repository, but in the case that the disclaimer changes, it can be found here: https://catalog.data.gov/dataset/event-correlated-outage-dataset-in-america
