# Predicting_Police_Activity


### Partners  
**Authors:**  

* [Renetta Nelson](https://github.com/RenettaNelson)
* [Salvador Sanchez Castro](https://github.com/zalvatore)
* [Ruddy Simonpour](https://github.com/ruddysimon) 

<p align ="center">
<img src = "/Images/SDSA.png">
</p>

**Company Name:** SD Solution Analytics</br>
**Company Industry:** Predictive policing solution</br>
**Company Size:** 10 - 50

----

### Abstract 
SD Analytics Solution (SDAS) is a data analysis company with a staff of 10-50 employees. The company has acquired a dataset of police stop data and information on police dispatches. The project will apply feature engineering techniques to select and transform essential features representing the data, preparing it for use in predicting future dispatches using various machine learning models. The project will employ multiple evaluation metrics to assess the accuracy of the models. Additionally, the project will seek to identify actionable insights for law enforcement personnel, aimed at reducing the frequency of incidents. 

----

### Problem Statement
The San Diego Police Department's communications dispatch center handles emergency and non-emergency calls, with police dispatchers assessing the level and nature of police assistance required for each situation. Public safety telecommunications personnel monitor and track all calls, providing necessary resources to those in need. In this project, SD Analytics Solution will apply statistical analysis and modeling techniques to the call data in order to identify trends and patterns. The objective is to provide more accurate and efficient police response to emergency and non-emergency situations by analyzing various elements of the calls. Additionally, the project aims to predict future dispatches using these models, enabling proactive measures to be taken to prevent incidents. This analysis has the potential to improve public safety by enhancing the effectiveness of police procedures and ensuring appropriate resources are allocated in a timely and efficient manner.

----

### Data Resources
* [Police Calls for Service - City of San Diego Open Data Portal](https://data.sandiego.gov/datasets/police-calls-for-service/)
* [PRIPA police stop data - basic details - City of San Diego Open Data Portal](https://data.sandiego.gov/datasets/police-ripa-stops/)
* [Police Calls for Service Call Types - City of San Diego Open Data Portal](https://data.sandiego.gov/datasets/police-calls-call-types/)

----

### Goals:
* Forecast the number of police calls per hour, identify peak times
* Forecast the police stops per day
* Predict the priority of a call
* Analyze the priority of calls in weekday and weekend comparisons

----

### AWS Config:
Public Bucket = 'sdpd-bucket'

----

### Process:
* Ingest Data -> https://seshat.datasd.org/pd/
* Data Storage -> Data Storage in S3 Bucket and Retrieval for Analysis
* Database and Table Structures -> AWS Athena
* Data Cleaning -> Detect Missing Values, Fixing Data Types, Feature Engineering, Encoding
* Data Modeling -> Classification, Time Series 
* Models ->

    1. DeepAR -> Forecast Number of Police Calls by hour
    2. Clasification -> Predict Prioirity of Police Calls 
    3. Time Series Forecast -> Forecast Number of Police Stops
    
----

## Model 1  Predicitng Calls for Police Service

#### Time Series Training and Testing

<p align ="center">
<img src = "/Images/police_calls_train_test.png">
</p>


#### Original RSME-> 10.6 Calls per Hour

<p align ="center">
<img src = "/Images/Training _Jobs_RSME.png">
</p>

#### HyperTuned RSME-> 8.6 Calls per Hour

<p align ="center">
<img src = "/Images/police_calls_forecast.png">
</p>

#### Plotly Figure using AWS Endpoint

<p align ="center">
<img src = "/Images/Plotly_Forecast.png">
</p>
