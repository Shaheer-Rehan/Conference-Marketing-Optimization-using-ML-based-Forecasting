# Conference Marketing Optimization using ML-based Forecasting

## Project Overview
This project is designed to predict event bookings and attendance using an Elastic Net Regression model and a graphical user interface (GUI) built with Tkinter. The system allows event organizers to input event-related data and receive predictions on the total number of bookings and expected attendance for their event. Predictions are provided both with and without advertisement campaigns, giving users insights into how marketing efforts could influence their event's success.

This repository contains the python script files for the comparative study of different machine learning models tested for the purposes of forecasting conference registration numbers using the available data. The Elastic Net Regression model was the one that performed the best, and so it is the model that is used in the **Prediction Model and GUI** folder of this repository. All other folders contain script files for different stages of the project like data analysis, comparative study of the prediction models, and imputation of missing data, to provide transparency into the workflow. 

For the end-user application, only the **Prediction Model and GUI** folder is of importance.

## Key Features:
- Predict total bookings for an event.
- Predict expected attendance based on historical data.
- Simulate the effect of advertisement campaigns on bookings.
- User-friendly GUI for entering event details and displaying results.

## Installation
To set up the project locally, follow these steps:
1. Clone the repository:  
git clone https://github.com/Shaheer-Rehan/Conference-Marketing-Optimization-using-ML-based-Forecasting.git  
cd Conference-Marketing-Optimization-using-ML-based-Forecasting
2. Install the required dependencies. These include:  
- Python 3.8+
- Tkinter (for GUI)
- pandas
- scikit-learn (v1.4.0)
- datetime (v5.4)

## How It Works
### Model Training:
The Elastic Net Regression model is used to train on event-related data and booking counts. The dataset includes features like the number of days remaining until the event and advertisement status. The model is trained to predict booking counts and the effect of advertisement campaigns on booking numbers.
- **ElasticNetCV** is used to select the optimal alpha and l1_ratio for the regression model.
- Predictions are generated for both scenarios: with and without advertisements.

### GUI Overview:
The GUI allows users to input:
- Start Date (dd/mm/yyyy)
- Event Date (dd/mm/yyyy)
- Current Date (dd/mm/yyyy)
- Current Number of Bookings
- Target Audience (e.g., IT Managers, Property Managers, etc.)  

Upon submission, the model generates predictions, including:
- Total Predicted Bookings without advertisement.
- Total Predicted Bookings with advertisement.
- Expected Attendance based on historical trends.

### Backend Files:
1. **DataPrep.py:** Responsible for preparing and preprocessing the event data.
2. **FinalModel.py:** Contains the model logic for Elastic Net Regression.
3. **GUI.py:** Contains the script to launch the GUI window.
4. **CSV Files:** The csv files in the **Prediction Model and GUI** folder are required for to extract the event data and train the model.
5. **Software Guide.pdf:** This file contains basic instructions on how to use the application, and again lists all the files needed for the application to work properly. All the required files are present in the **Prediction Model and GUI** folder.

## Repository Folders
- **Classification Models:** Contains the Python scripts for the classification models (Logistic Regression, Decision Trees, Random Forests) that were used to try and predict the number of registrations of an event.
- **Data Analysis:** Contains a Python script to analyze the raw data to give an insight on the data set.
- **Data Imputation:** Contains the Python scripts for the Imputation techniques that were compared to assess which method showed best performance for handling the missing data. The techniques used for this were linear regression, logistic regression, mode, and KNN.
- **Prediction Model and GUI:** Contains the Python scripts for the final application, the GUI window, and the required csv files.
- **Regression Models:** Contains the Python scripts for the regression models (OLS Linear Regression, Elastic Net Regression, Regression Trees) that were used to try and predict the number of registrations of an event.
- **Time Series Models:** Contains the Python scripts for the time series models (ARIMA, SARIMAX, Exponential Smoothing) that were used to try and predict the number of registrations of an event.
