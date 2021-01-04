# Operationalizing Machine Learning

## Table of Contents
* ### Overview
* ### Architectural Diagram
* ### Key Steps
     * Automated ML Experiment 
     * Deploy the best model
     * Enable App Insights & Logging
     * Swagger Documentation
     * Consume model endpoints
     * Create and publish a pipeline
* Screen Recording
* Standout Suggestions
* References

## Overview
This projects aims to create a cloud-based machine learning model for the Bank Marketing Dataset, which contains data about marketing campaigns for a bank, to create this model we will utilize the power of AutoML for this classification problem to be able to predict whether a bank product would be subscribed by the client or not.  
The project involves configuring, deploying and consuming the model.
The project also includes creating, consuming and publishing an ML Pipeline.

## Architectural Diagram
The diagram below shows the operations done in the project from the start to finish.
*TODO*: Provide an architectual diagram of the project and give an introduction of each step. 

## Key Steps

### Step 1: Automated ML Experiment
In this step, we first upload our dataset using the dataset's URI:
![Dataset](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/Registered%20data%20sets.PNG)  

Then we use this data to create an AutoML run to determine the best model:
![Complete Run](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/complete%20run.PNG)  

After the run is complete, we're able to determine the best model which is the **Voting Ensemble** with accuracy of **0.91866**:
![Best Model](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/best%20model.PNG)  

### Step 2: Deploy the best model
In this step, we deply the Voting Ensemble model using Azure Container Instacne (ACI) while making sure that the Authentication option enabled.
![Deployment](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/deploy.png)  


### Step 3: Enable App Insights & Logging
We enable the Application Insights by editing the logs.py script to match the deployed model ID and setting App Inights to ***True*** then we run the python script.
![App Insights](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/App%20insights%20enabled.PNG)  

Running logs.py after editing it:
![Logs](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/enabling%20logs.PNG) 

Screenshots of Logs:
![Logs](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/logs1.PNG) 
![Logs](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/logs2.PNG) 

### Step 4: Swagger Documentation
In this step we setup Swagger to be able to deploy and consume the model using Swagger.
We start by download the swagger.json file from our deployed model on Azure. Then we run swagger.sh and serve.py script on Powershell command window.
Swagger on localhost:  
![Swagger](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/swagger%20methods.PNG) 
![Swagger](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/swagger%20screenshots%202.PNG) 
![Swagger](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/instance%20interaction%202.PNG) 
![Swagger](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/swagger%20screenshots.PNG) 

### Step 5: Consume model endpoints  
Using the endpoint.py script to consume the model endpoints, we first edit the *scoring_uri* and the *key* in the script to match the key for your service and the URI that was generated after deployment, then we execute endpoint.py script.
![Endpoint](https://github.com/dinaabdulrasoul/Operationalizing-Machine-Learning/blob/main/screenshots/endpoint.png) 

### Step 6: Create and publish a pipeline

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
