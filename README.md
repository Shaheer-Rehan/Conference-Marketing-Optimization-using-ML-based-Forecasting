# Conference Marketing Optimization using ML-based Forecasting

## Project Overview
This project is designed to predict event bookings and attendance using an Elastic Net Regression model. The system allows event organizers to input event-related data and receive predictions on the total number of bookings expected for their event. Predictions are provided both with and without advertisement campaigns, giving users insights into how marketing efforts could influence their event's success.

This repository contains the Python script file **DataPrep.py** for data preprocessing, the **PredictionModelPerformance.ipynb** file analysing the performance of the Elastic Net Regression model for the task of predicting event bookings, and the **FinalPredictionModel.ipynb** notebook which allows users to interact with the prediction model to carry out predictions for any future/current event. The model is based on event data from an industrial client, and as such, is tailored for the use case of said client, however, by adding .csv files with formatting consistent to the existing ones, the database for the prediction model can be expanded to achieve more generic results. 

The Elastic Net Regression model was selected after performing a comparative study of several candidate models, including other regression and time series ML models. 

## Key Features:
- Predict total bookings for an event based on current registration/booking counts.
- Simulate the effect of advertisement campaigns on bookings.

## Installation
To set up the project locally, follow these steps:
1. Clone the repository:  
git clone https://github.com/Shaheer-Rehan/Conference-Marketing-Optimization-using-ML-based-Forecasting.git  
cd Conference-Marketing-Optimization-using-ML-based-Forecasting
2. Install the required dependencies. These include:  
- Python 3.8+
- pandas
- scikit-learn (v1.4.0)
- datetime (v5.4)

## How It Works
### Model Training:
The Elastic Net Regression model is used to train on event-related data and booking counts. The dataset includes features like the number of days remaining until the event and advertisement status. The model is trained to predict booking counts and the effect of advertisement campaigns on booking numbers.
- **ElasticNetCV** is used to select the optimal alpha and l1_ratio for the regression model.
- Predictions are generated for both scenarios: with and without advertisements.

### User Interface:
The User Interface allows users to input:
- Start Date (dd/mm/yyyy)
- Event Date (dd/mm/yyyy)
- Current Date (dd/mm/yyyy)
- Current Number of Bookings
- Target Audience (e.g., IT Managers, Property Managers, etc.)  

Upon submission, the model predicts the total number of bookings up to the Event Date.

### Backend Files:
1. **DataPrep.py:** Responsible for preparing and preprocessing the event data.
2. **CSV Files:** The .csv files in the **Prediction Model and GUI** folder are required to extract the event data and train the model.
