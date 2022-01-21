# Recommendation-Systems-for-IBM-Watson-Studio-platform

### Project Overview
In this project, I analyze the interactions that users have with articles on the IBM Watson Studio platform, and recommend new articles to them.

### Project Components
There are three components you'll need to complete for this project.

1. ETL Pipeline
 The ETL pipeline is included in "process_data.py" file and performs following tasks:
    - Loads the messages from disaster_messages.csv and data/disaster_categories.csv datasets.
    - Merges the two datasets.
    - Cleans the data.
    - Stores it in a SQLite database.

2. ML Pipeline
 The ML pipeline is included in "train_classifier.py" file and performs following tasks:
    - Loads data from the SQLite database.
    - Splits the dataset into training and test sets.
    - Builds a text processing and machine learning pipeline.
    - Trains and tunes a model using GridSearchCV.
    - Outputs results on the test set.
    - Exports the final model as a pickle file.

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/disaster_response_db.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/disaster_response_db.db models/classifier.pkl`
### Files In The Repository:
#### app:      
| - template.     
| |- master.html # main page of web app.     
| |- go.html # classification result page of web app.     
|- run.py # Flask file that runs app.      
#### data:   
|- disaster_categories.csv # data to process.     
|- disaster_messages.csv # data to process.  
|- process_data.py. 
|- disaster_response_db.db # database to save clean data to.  
#### models:   
|- train_classifier.py.  
|- classifier.pkl # saved model.    
#### README.md
