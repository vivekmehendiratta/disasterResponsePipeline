# Installation

    Python 3.6.*
    Flask
    Plotly

# Project Motivation
For this project, I incorporated back-end and front-end skills to analyse disaster response data from APPEN to build a model that classifies disaster response messages. I used Flask framework to develop a dashboard that shows the category in which the message lies.

# Files Description

    ├── app     
    │   ├── run.py                           
    │   └── templates   
    │       ├── go.html                      
    │       └── master.html                    
    ├── data
    |   ├── disasterResponse.db
    │   ├── disaster_categories.csv           
    │   ├── disaster_messages.csv            
    │   └── process_data.py                  
    └── models
        ├── classifier.pkl
        └── train_classifier.py                       
    
    
 # Instructions
 1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
